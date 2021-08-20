---
description: Recupera um código que identifica o tipo de exceção que ocorre. A função pode ser chamada somente de dentro da expressão de filtro ou do bloco manipulador de exceção de um manipulador de exceção.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: Macro GetExceptionCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5c1badd5317b5a12eb97ed6418873b5c576f520f4a8106361abb1a6f7c95921e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162657"
---
# <a name="getexceptioncode-macro"></a>Macro GetExceptionCode

Recupera um código que identifica o tipo de exceção que ocorre. A função pode ser chamada somente de dentro da expressão de filtro ou do bloco manipulador de exceção de um manipulador de exceção.

> [!Note]  
> O compilador de otimização do Microsoft C/C++ interpreta essa função como uma palavra-chave e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parâmetros

Esta macro não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O valor de retorno identifica o tipo de exceção. A tabela a seguir identifica os códigos de exceção que podem ocorrer devido a erros comuns de programação. Esses valores são definidos em WinBase. h e WinNT. h.



| Código de retorno                                                                                                         | Descrição                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_violação de acesso à exceção \_**</dt> </dl>         | O thread tenta ler ou gravar em um endereço virtual para o qual ele não tem acesso.<br/> Esse valor é definido como violação de acesso de STATUS \_ \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**limites de matriz de exceção \_ \_ \_ excedidos**</dt> </dl>   | O thread tenta acessar um elemento de matriz que está fora dos limites e o hardware subjacente dá suporte à verificação de limites.<br/> Esse valor é definido como limites de matriz de STATUS \_ \_ \_ excedidos.<br/>                                                                                                                 |
| <dl> <dt>**ponto de interrupção de exceção \_**</dt> </dl>                | Um ponto de interrupção foi encontrado.<br/> Esse valor é definido como ponto de interrupção de STATUS \_ .<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**inalinhamento de DataType de exceção \_ \_**</dt> </dl>    | O thread tenta ler ou gravar dados que estão desalinhados em hardware que não fornece alinhamento. Por exemplo, valores de 16 bits devem ser alinhados em limites de 2 bytes, valores de 32 bits em limites de 4 bytes e assim por diante.<br/> Esse valor é definido como estado de tipo de dados de STATUS \_ \_ desalinhado.<br/>                    |
| <dl> <dt>**EXCEÇÃO \_ do \_ operando DENORMAL de FLT \_**</dt> </dl>    | Um dos operandos em uma operação de ponto flutuante é desnormal. Um valor desnormal é um que é muito pequeno para representar como um valor de ponto flutuante padrão.<br/> Esse valor é definido como um \_ operando de status float \_ desnormal \_ .<br/>                                                                                  |
| <dl> <dt>**EXCEÇÃO \_ FLT \_ \_ de divisão por \_ zero**</dt> </dl>     | O thread tenta dividir um valor de ponto flutuante por um divisor de ponto flutuante de 0 (zero).<br/> Esse valor é definido como STATUS \_ float \_ divide \_ por \_ zero.<br/>                                                                                                                                               |
| <dl> <dt>**resultado de FLT de exceção \_ \_ inexata \_**</dt> </dl>      | O resultado de uma operação de ponto flutuante não pode ser representado exatamente como uma fração decimal.<br/> Esse valor é definido como resultado de float de STATUS \_ \_ inexato \_ .<br/>                                                                                                                                                |
| <dl> <dt>**EXCEÇÃO de \_ operação de FLT \_ inválida \_**</dt> </dl>   | Uma exceção de ponto flutuante que não está incluída nesta lista.<br/> Esse valor é definido como uma \_ operação de status float \_ inválida \_ .<br/>                                                                                                                                                                             |
| <dl> <dt>**\_estouro de FLT de exceção \_**</dt> </dl>             | O expoente de uma operação de ponto flutuante é maior do que a magnitude permitida pelo tipo correspondente.<br/> Esse valor é definido como overflow de STATUS \_ float \_ .<br/>                                                                                                                                         |
| <dl> <dt>**EXCEÇÃO \_ de \_ verificação de pilha FLT \_**</dt> </dl>         | A pilha estourou ou excedeu o estouro devido a uma operação de ponto flutuante.<br/> Esse valor é definido como verificação de pilha de STATUS \_ flutuante \_ \_ .<br/>                                                                                                                                                                 |
| <dl> <dt>**\_estouro negativo de FLT de exceção \_**</dt> </dl>            | O expoente de uma operação de ponto flutuante é menor que a magnitude permitida pelo tipo correspondente.<br/> Esse valor é definido como STATUS \_ de \_ estouro negativo.<br/>                                                                                                                                           |
| <dl> <dt>**\_página de proteção de exceção \_**</dt> </dl>               | O thread acessou a memória alocada com o \_ modificador de proteção de página.<br/> Esse valor é definido como violação de página de proteção de STATUS \_ \_ \_ .<br/>                                                                                                                                                                          |
| <dl> <dt>**instrução de exceção \_ ilegal \_**</dt> </dl>      | O thread tenta executar uma instrução inválida.<br/> Esse valor é definido como instrução de STATUS \_ inválido \_ .<br/>                                                                                                                                                                                            |
| <dl> <dt>**EXCEÇÃO \_ em \_ erro de página \_**</dt> </dl>           | O thread tenta acessar uma página que não está presente e o sistema não consegue carregar a página. Por exemplo, essa exceção pode ocorrer se uma conexão de rede for perdida durante a execução de um programa em uma rede.<br/> Esse valor é definido como STATUS \_ em \_ erro de página \_ .<br/>                                   |
| <dl> <dt>**EXCEÇÃO \_ int \_ dividir \_ por \_ zero**</dt> </dl>     | O thread tenta dividir um valor inteiro por um divisor inteiro de 0 (zero).<br/> Esse valor é definido como o \_ inteiro de status \_ divisão \_ por \_ zero.<br/>                                                                                                                                                         |
| <dl> <dt>**\_estouro de int de exceção \_**</dt> </dl>             | O resultado de uma operação de inteiro cria um valor muito grande para ser mantido pelo registro de destino. Em alguns casos, isso resultará em uma execução do bit mais significativo do resultado. Algumas operações não definem o sinalizador de transporte.<br/> Esse valor é definido como estouro de inteiro de STATUS \_ \_ .<br/> |
| <dl> <dt>**\_disposição inválida da exceção \_**</dt> </dl>      | Um manipulador de exceção retorna uma disposição inválida para o Dispatcher de exceção. Os programadores que usam uma linguagem de alto nível, como C, nunca devem encontrar essa exceção.<br/> Esse valor é definido como o STATUS de \_ disposição inválida \_ .<br/>                                                                      |
| <dl> <dt>**\_identificador inválido da exceção \_**</dt> </dl>           | O thread usou um identificador para um objeto de kernel inválido (provavelmente porque ele tinha sido fechado).<br/> Esse valor é definido como \_ identificador inválido de status \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**exceção \_ não continuável de exceção \_**</dt> </dl> | O thread tenta continuar a execução após a ocorrência de uma exceção não continuável.<br/> Esse valor é definido como a \_ exceção de não continuável de status \_ .<br/>                                                                                                                                                       |
| <dl> <dt>**\_instrução priv de exceção \_**</dt> </dl>         | O thread tenta executar uma instrução com uma operação que não é permitida no modo de computador atual.<br/> Esse valor é definido como instrução de STATUS \_ privilegiado \_ .<br/>                                                                                                                           |
| <dl> <dt>**\_etapa única de exceção \_**</dt> </dl>              | Uma interceptação de rastreamento ou outro mecanismo de instrução único sinaliza que uma instrução é executada.<br/> Esse valor é definido como \_ uma etapa de status único \_ .<br/>                                                                                                                                                           |
| <dl> <dt>**\_estouro de pilha de exceção \_**</dt> </dl>           | O thread usa sua pilha.<br/> Esse valor é definido como estouro de pilha de STATUS \_ \_ .<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**liberação de STATUS de \_ \_ desconsolidação**</dt> </dl>          | Uma consolidação de quadros foi executada.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentários

A função **GetExceptionCode** pode ser chamada somente de dentro da expressão de filtro ou do bloco de manipulador de exceção de um manipulador de exceção. A expressão de filtro será avaliada se ocorrer uma exceção durante a execução do bloco **\_ \_ try** e determinar se o bloco **\_ \_ Except** será ou não executado.

A expressão de filtro pode invocar uma função de filtro. A função Filter não pode chamar **GetExceptionCode**. No entanto, o valor de retorno de **GetExceptionCode** pode ser passado como um parâmetro para uma função de filtro. O valor de retorno da função [**GetExceptionInformation**](getexceptioninformation.md) também pode ser passado como um parâmetro para uma função de filtro. **GetExceptionInformation** retorna um ponteiro para uma estrutura que inclui as informações de código de exceção.

Quando há manipuladores aninhados, cada expressão de filtro é avaliada até que uma seja avaliada como exceção de \_ \_ execução de manipulador ou de continuação de exceção \_ \_ . Cada expressão de filtro pode invocar **GetExceptionCode** para obter o código de exceção.

O código de exceção retornado é o código gerado por uma exceção de hardware ou o código especificado na função [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) para uma exceção gerada pelo software.

Ao manipular a exceção de ponto de interrupção, é importante incrementar o ponteiro de instrução no registro de contexto para continuar a partir dessa exceção.

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [usando um manipulador de exceção](using-an-exception-handler.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Funções de manipulação de exceção estruturada](structured-exception-handling-functions.md)
</dt> <dt>

[Visão geral da manipulação de exceção estruturada](structured-exception-handling.md)
</dt> </dl>

 

 
