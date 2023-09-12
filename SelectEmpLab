package day18;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.Statement;
import java.util.Random;

public class SelectEmpLab {

	public static void main(String[] args) throws Exception {
		String url = "jdbc:mysql://localhost:3306/edudb?characterEncoding=UTF-8&serverTimezone=UTC";
		String user = "jdbctest";
		String passwd = "jdbctest";
		Connection conn = DriverManager.getConnection(url, user, passwd);
		Statement stmt = conn.createStatement();
		ResultSet rs = stmt.executeQuery("select ename, format(sal,0) fsal, year(hiredate) y,month(hiredate) m,day(hiredate) d from emp");
		Random rand = new Random();
		boolean ft = rand.nextBoolean();
		if(ft) {
			while(rs.next()) {
				System.out.printf("%s 직원의 월급은 %s달러입니다.\n",rs.getString("ename"),rs.getString("fsal"));
			}
		}else {
			while(rs.next()) {
				System.out.printf("%s 직원은 %d년 %d월 %d일에 입사하였습니다.\n",rs.getString("ename"),rs.getInt("y"),rs.getInt("m"),rs.getInt("d"));
			}
		}
		rs.close();
		stmt.close();
		conn.close();
	}
}
