# firststeps_php
*________________________________________________________________________________________________________________________________________*
*feito para uma hipotese que exista um vendedor com dois montantes:

salário = valor total a ser recebido
vendas = comissão de 15% a ser recebida em cima do montante total de vendas
*________________________________________________________________________________________________________________________________________*

<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <title> Formulário Salário </title>
	</head>
	<body>
		<h3>Vendas + Salário Fixo</h3>
		<form method = "POST" action = "#">
			<label>Vulgo do Menor: </label>
			<input type="text" required name = "txt_nome">

            <BR><BR>
	
			<label>Pataco: </label>
			<input type="text" required name = "txt_salario">

            <BR><BR>
			
			<label>Vendas: </label>
			<input type="text" required name = "txt_vendas">

            <BR><BR>

	<input type ="submit" name="btn_exibir" value="Pataco Final">  
	</form>

	<?php

    if (count($_POST))

    {
	$nome = $_POST ["txt_nome"];
	$salario = $_POST ["txt_salario"];
	$vendas = $_POST ["txt_vendas"];
	$salariof;
    $porcentagem;
    $porcentagem = $vendas / "100" * "15";   
	$salariof = $salario + $porcentagem;
   
	echo "<br> Resultado: ".$salariof;
    }
	?>

	</body>
</html>
