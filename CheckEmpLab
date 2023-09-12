package day18;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.Statement;
import java.util.Scanner;

public class CheckEmpLab {

	public static void main(String[] args) throws Exception{
		String url = "jdbc:mysql://localhost:3306/edudb?characterEncoding=UTF-8&serverTimezone=UTC";
		String user = "jdbctest";
		String passwd = "jdbctest";
		Connection conn = DriverManager.getConnection(url, user, passwd);
		Statement stmt = conn.createStatement();
		ResultSet rs;
		Scanner sc = new Scanner(System.in);
		String name;
		boolean search;
		while(true) {
			rs = stmt.executeQuery("select ename,  year(hiredate) y,month(hiredate) m,deptno from emp");
			search=false;
			System.out.print("직원의 이름(종료를 원하시면 x를 입력하시오) : ");
			name = sc.next();
			if(name.equals("x")) {
				break;
			}
			while(rs.next()) {
				if(name.equals(rs.getString("ename"))) {
					System.out.printf("%s 직원은 근무중입니다.\n",rs.getString("ename"));
					System.out.printf("%s 직원은 %d년 %d월에 입사했고 현재 %d번 부서에서 근무하고 있습니다.\n",rs.getString("ename"),rs.getInt("y"),rs.getInt("m"),rs.getInt("deptno"));
					search=true;
				}
			}
			if(!search) {
				System.out.printf("%s 직원은 근무하지 않습니다.\n",name);
				break;
			}
		}
		System.out.println("종료되었습니다.");
		sc.close();
	}
}
