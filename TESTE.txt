package teste.senai;

import java.sql.Driver;

import org.junit.After;
import org.junit.Before;
import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class TesteCursoSenai {
	
	private WebDriver driver;
	
	// inicio
	@Before
	public void ConfigurarTeste () {
		System.setProperty("webdriver.chrome.driver", "C:\\Program Files\\ChromeDriver\\chromedriver.exe");
		driver = new ChromeDriver() ;
		driver.manage().window().maximize();
		//driver.quit();
	}
	
	
	
	//teste
	@Test
	public void TesteNavegabilidade () {
		driver.get("https://informatica.sp.senai.br/");
		driver.findElement(By.id("Busca1_txtFiltro")).sendKeys("programação");
		driver.findElement(By.id("Busca1_btnBusca")).click(); 
	}
	
	//finalização
	// @After
	
	
	
	
}
