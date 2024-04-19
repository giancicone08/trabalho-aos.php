# trabalho-aos.php
//ex 1
  <?php

$produto =   [
produto" => "Camisa DnD - Tamanho M",
"data_pagamento" => "01/02/2024",
"pago" => false
 ];
 function vedata($produto){

 if($produto["data_pagamento"]<"02/02/2024"){
  $produto["pago"] => true;

  var_dump($produto);

  }else{
  $produto["pago"] => false;

  vardump($produto);
  }


  //ex 2 
   $escola = [
     [
        "produto" => "Camisa DnD - Tamanho M",
        "data_pagamento" => "01/02/2024",
        "pago" => false
    ];

    function($escola){
    $media = array_sum($notas)/2;
    echo "a media é {'$media'};
    };

    //ex 3 
    
$nomes =  [
        [
            "nome" => "João",
            "idade" => 20
        ],
        [
            "nome" => "Maria",
            "idade" => 22
        ],
        [
            "nome" => "José",
            "idade" => 21
        ]
    ];
    
    function ($nomes){
        $idade = array_sum($nomes)
        echo 'mostrar os {'$nomes'}'
    }

    //ex4
    $usuarios = [
    [
        "nome" => "João",
        "idade" => 20,
        "email" => "email@email.com",
        "senha" => "12345678"
    ],
    [
        "nome" => "Guilherme",
        "idade" => 17,
        "email" => "meu.email@email.com",
        "senha" => "abc12312312"
    ]
];

function verificarCadastro($novoUsuario, &$usuarios) {
    if (strlen($novoUsuario["nome"]) <= 3) {
        echo "Erro: O nome deve ter mais de 3 caracteres.\n";
        return false;
    }
    if ($novoUsuario["idade"] <= 18) {
        echo "Erro: A idade deve ser maior que 18.\n";
        return false;
    }
    if (strlen($novoUsuario["email"]) <= 10) {
        echo "Erro: O e-mail deve ter mais de 10 caracteres.\n";
        return false;
    }
    if (strlen($novoUsuario["senha"]) <= 8) {
        echo "Erro: A senha deve ter mais de 8 caracteres.\n";
        return false;
    }
    foreach ($usuarios as $usuario) {
        if ($usuario["email"] === $novoUsuario["email"]) {
            echo "Erro: O e-mail já está cadastrado.\n";
            return false;
        }
    }
    $usuarios[] = $novoUsuario;
    echo "Usuário cadastrado com sucesso!\n";
    return true;
}

// Exemplo de uso:
$novoUsuario = [
    "nome" => "Ana",
    "idade" => 25,
    "email" => "ana.email@provedor.com",
    "senha" => "senhaSegura123"
];

verificarCadastro($novoUsuario, $usuarios);

echo ($usuarios);

?>
    
