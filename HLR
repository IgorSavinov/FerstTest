import org.junit.Assert;
import org.junit.Test;
import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

import java.util.ArrayList;
import java.util.List;

import static org.openqa.selenium.support.ui.ExpectedConditions.alertIsPresent;

public class TestHLR extends WebDriverSetting {

    @Test
    public void TestHLR () throws InterruptedException {
        driver.get("https://ng.unitedline.net/");

        driver.manage().window().maximize();

        WebDriverWait singIn = new WebDriverWait(driver, 20);
        singIn.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//a[@class='sign-in'])"))) ;
        //клик на кнопку логин
        WebElement login = driver.findElement(By.xpath("(//a[@class='sign-in'])"));
        login.click();
        //ожидание полей ввода
        WebDriverWait mail = new WebDriverWait(driver, 20);
        mail.until(ExpectedConditions.visibilityOfElementLocated(By.name("email"))) ;
        //ввод логин пароль
        driver.findElement(By.name("email")).sendKeys("savinov@didlogic.com");

        driver.findElement(By.name("password")).sendKeys("simplepass");

        driver.findElement(By.xpath("(//input[@class='submit'])[1]")).click();

        // загрузка старницы выбора стран
        WebDriverWait waitHeaderBuy = new WebDriverWait(driver, 10);
        waitHeaderBuy.until(ExpectedConditions.visibilityOfElementLocated(By.className("header-wrapper"))) ;

        //переход в админку
        Thread.sleep(5000);
        driver.get("https://ng.unitedline.net/admin");

        //клик по кнопке админ
        driver.findElement(By.xpath("(//a)[1]")).click();

        //клик по HLR
        driver.findElement(By.xpath("//a[@href='/admin/hlr']")).click();

        WebDriverWait country = new WebDriverWait(driver, 20);
        country.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//select[@id='hlr_country_hlr_supplier']"))) ;
        driver.findElement(By.xpath("//select[@id='hlr_country_hlr_supplier']")).click();

        //клик по андоре
        WebDriverWait angolaWait = new WebDriverWait(driver, 20);
        angolaWait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//option[@value='AO']"))) ;

        driver.findElement(By.xpath("//option[@value='AO']")).click();
        //клик по рандомной стране
        driver.findElement(By.xpath("(//td[@class='th-hlr-table-country'])[1]")).click();

        //клик по дропдауну Default HLR Lookup supplier
        WebDriverWait defaultHLR = new WebDriverWait(driver, 20);
        defaultHLR.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//div[@class='supplier text-field-medium']")));
        driver.findElement(By.xpath("//select[@id='hlr_country_hlr_supplier_id']")).click();

        //клик по ланк
        WebDriverWait lank = new WebDriverWait(driver, 20);
        lank.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//option[@value='3']"))) ;
        driver.findElement(By.xpath("//option[@value='3']")).click();

        //клик по рандомной стране
        driver.findElement(By.xpath("(//td[@class='th-hlr-table-country'])[1]")).click();

        //клик по кнопке аддконтри
        driver.findElement(By.xpath("//span[@class='new_hlr_country_action-registry']")).click();

        //клик по кнопке едит
        WebDriverWait edit = new WebDriverWait(driver, 20);
        edit.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//p[@class='hlr-country__action-edit'])[last()]"))) ;

        WebElement editButton = driver.findElement(By.xpath("(//p[@class='hlr-country__action-edit'])[last()]"));
        JavascriptExecutor executorEditButton = (JavascriptExecutor)driver;
        executorEditButton.executeScript("arguments[0].click();", editButton);

        //клик по дропдауну
        driver.findElement(By.xpath("//select[@id=\"hlr_country_hlr_supplier_id\"]")).click();

        //клик для смены сети в дропдауне
        driver.findElement(By.xpath("//option[@value='4']")).click();

        //клиу по сейв
        driver.findElement(By.xpath("//span[@class='hlr-country__action-save']")).click();
        Thread.sleep(2000);

        //клик по дизейбл
        WebElement disableButton = driver.findElement(By.xpath("(//a[@class='hlr-country__action-disabled'])[last()]"));
        JavascriptExecutor executorDisableButton = (JavascriptExecutor)driver;
        executorDisableButton.executeScript("arguments[0].click();", disableButton);

        //клик по алерту
        WebDriverWait enable = new WebDriverWait(driver, 200);
        Alert alert = enable.until(alertIsPresent());
        alert.accept();

        //клик по кнопке енейбл
        WebDriverWait enableButtonWait = new WebDriverWait(driver, 20);
        enableButtonWait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//a[@class='hlr-country__action-enable'])[last()]"))) ;

        WebElement enableButton = driver.findElement(By.xpath("(//a[@class='hlr-country__action-enable'])[last()]"));
        JavascriptExecutor executorEnableButton = (JavascriptExecutor)driver;
        executorEnableButton.executeScript("arguments[0].click();", enableButton);

        //клик по копке делет
        WebDriverWait deleteButtonWait = new WebDriverWait(driver, 20);
        deleteButtonWait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//a[@data-method='delete'])[last()]"))) ;

        WebElement deleteButton = driver.findElement(By.xpath("(//a[@data-method='delete'])[last()]"));
        JavascriptExecutor executorDeleteButton = (JavascriptExecutor)driver;
        executorDeleteButton.executeScript("arguments[0].click();", deleteButton);

        //клик по алекту
        WebDriverWait delete = new WebDriverWait(driver, 200);
        Alert alertDelete = delete.until(alertIsPresent());
        alertDelete.accept();


       driver.findElement(By.xpath("//a[@class='subnav']")).click();

       //клик по дропдауну кантри
        driver.findElement(By.xpath("//select[@id='hlr_connection_hlr_country_id']")).click();

        driver.findElement(By.xpath("/html/body/div[1]/div[4]/div/div/div/div/form/ul/li[1]/div[2]/select/option[4]")).click();

        //клик по случайно стране
        driver.findElement(By.xpath("//td[@class=\"th-hlr-table-country\"]")).click();

        //клик по дропдауну
        driver.findElement(By.xpath("//select[@id='hlr_connection_carrier_index']")).click();

        driver.findElement(By.xpath("//option[@value='633']")).click();

        //клик по случайно стране
        driver.findElement(By.xpath("//td[@class=\"th-hlr-table-country\"]")).click();

        //клик по чекбоксам
        driver.findElement(By.xpath("(//div[@class='field-checkbox'])[1]")).click();

        driver.findElement(By.xpath("(//div[@class='field-checkbox'])[1]")).click();

        driver.findElement(By.xpath("(//div[@class='field-checkbox'])[1]")).click();

        driver.findElement(By.xpath("(//div[@class='field-checkbox'])[1]")).click();

        //клик по кнопке греейд
        driver.findElement(By.xpath("//span[@class='hlr-connection__action-create']")).click();

        //ожидание чекбокса
        WebDriverWait checkboxTyntecWait = new WebDriverWait(driver, 20);
        checkboxTyntecWait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//td[contains(text(),'Yes')])[20]"))) ;

        //клик по чекбоксам
        String  checkboxTyntec = driver.findElement(By.xpath("(//td[contains(text(),'Yes')])[20]")).getText();
        System.out.println(checkboxTyntec);
        Assert.assertEquals(checkboxTyntec,"Yes");

        String  checkboxXConnect = driver.findElement(By.xpath("(//td[contains(text(),'Yes')])[20]")).getText();
        System.out.println(checkboxXConnect);
        Assert.assertEquals(checkboxXConnect,"Yes");

        String  checkboxLanck = driver.findElement(By.xpath("(//td[contains(text(),'Yes')])[20]")).getText();
        System.out.println(checkboxLanck);
        Assert.assertEquals(checkboxLanck,"Yes");

        String  checkboxMiatel = driver.findElement(By.xpath("(//td[contains(text(),'Yes')])[20]")).getText();
        System.out.println(checkboxMiatel);
        Assert.assertEquals(checkboxMiatel,"Yes");

        //клик по дезейбл MNO Routing
        WebDriverWait buttonDisableWait = new WebDriverWait(driver, 20);
        buttonDisableWait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//a[@class='hlr-connection__action-disabled'])[last()]"))) ;

        WebElement disableButtonMNO = driver.findElement(By.xpath("(//a[@class='hlr-connection__action-disabled'])[last()]"));
        JavascriptExecutor executorDisableButtonMNO = (JavascriptExecutor)driver;
        executorDisableButtonMNO.executeScript("arguments[0].click();", disableButtonMNO);


        //клмк по алерту
        WebDriverWait deleteMNO = new WebDriverWait(driver, 200);
        Alert alertDeleteMNO = deleteMNO.until(alertIsPresent());
        alertDeleteMNO.accept();
        //клик по енейбл MNO
        WebDriverWait buttonEnableMNOWait = new WebDriverWait(driver, 20);
        buttonEnableMNOWait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//a[@class='hlr-connection__action-enable'])[last()]")));

        WebElement enableButtonMNO = driver.findElement(By.xpath("(//a[@class='hlr-connection__action-enable'])[last()]"));
        JavascriptExecutor executorEnableButtonMNO = (JavascriptExecutor)driver;
        executorEnableButtonMNO.executeScript("arguments[0].click();", enableButtonMNO);

        WebElement enableButtonMNO1 = driver.findElement(By.xpath("(//a[@class='hlr-connection__action-enable'])[last()]"));
        JavascriptExecutor executorEnableButtonMNO1 = (JavascriptExecutor)driver;
        executorEnableButtonMNO1.executeScript("arguments[0].click();", enableButtonMNO1);
        //клик по кнопке едит
        //driver.findElement(By.xpath("(//a[@class='hlr-connection__action-enable'])[last()]")).click();








    }

}
