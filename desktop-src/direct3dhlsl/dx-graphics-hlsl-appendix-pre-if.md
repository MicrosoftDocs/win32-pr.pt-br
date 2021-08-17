---
title: " Diretivas if, elif, else e endif"
description: Diretivas de pré-processador que controlam a compilação de partes de um arquivo de origem.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Diretivas if, elif, else e endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb5f4716509905d4ce800abbe4cb11b85d116d7a5afd5a56301b1ecb5ce0724b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726446"
---
# <a name="if-elif-else-and-endif-directives"></a>\#Diretivas \# if, \# elif, else e \# endif

Diretivas de pré-processador que controlam a compilação de partes de um arquivo de origem.



| \#if *ifCondition* ...         |
|--------------------------------|
| \[\#elif *elifCondition...*\] |
| \[\#Mais...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condição primária a ser avaliada. Se esse parâmetro for avaliada como um valor diferente de zero, todo o texto entre essa diretiva if e a próxima instância da diretiva elif, else ou endif será mantido na unidade de \# \# \# tradução; caso contrário, o código-fonte subsequente não \# será mantido. <br/> A condição pode usar o operador de pré-processador definido para determinar se uma constante ou macro de pré-processador específica está definida; esse uso é equivalente ao uso da [ \# diretiva ifdef.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Consulte a seção Comentários para ver as restrições sobre o valor do *parâmetro ifCondition.* <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ Opcional\] <br/> | Outra condição a ser avaliada. Se o parâmetro *ifCondition* e todas as diretivas elif anteriores são avaliadas como zero e esse parâmetro é avaliada como um valor diferente de zero, todo o texto entre essa diretiva elif e a próxima instância da diretiva \# elif, else ou endif será mantido na unidade de tradução; caso contrário, o código-fonte subsequente não \# \# será \# \# mantido. <br/> A condição pode usar o operador de pré-processador definido para determinar se uma constante ou macro de pré-processador específica está definida; esse uso é equivalente ao uso da [ \# diretiva ifdef.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Consulte a seção Comentários para ver as restrições sobre o valor do *parâmetro elifCondition.* <br/> |



 

## <a name="remarks"></a>Comentários

Cada \# diretiva if em um arquivo de origem deve ser corresponder por uma diretiva \# endif de fechamento. Qualquer número de diretivas elif pode aparecer entre as diretivas if e \# endif, mas no máximo \# uma outra diretiva é \# \# permitida. A \# diretiva else, se presente, deve ser a última diretiva antes \# de endif. As diretivas de compilação condicional contidas em arquivos de inclusão devem atender às mesmas condições.

As \# diretivas if, elif, else e endif podem aninhar nas partes \# de texto de outras \# \# \# diretivas if. Cada diretiva \# else, \# elif ou \# endif aninhada pertence à diretiva if anterior \# anterior.

Se nenhuma condição for avaliada como um valor diferente de zero, o pré-processador selecionará o bloco de texto após a \# diretiva else. Se a cláusula else for omitida e nenhuma condição for avaliada como um valor diferente \# de zero, nenhum bloco de texto será selecionado.

Os *parâmetros ifCondition* *e elifCondition* atendem muito aos seguintes requisitos:

-   As expressões de compilação condicional são tratadas como valores [**longos**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) assinados e essas expressões são avaliadas usando as mesmas regras que as expressões em C++.
-   As expressões devem ter o tipo integral e podem incluir apenas constantes de inteiros, constantes de caracteres e o operador defined.
-   As expressões não podem **usar sizeof** ou um operador type-cast.
-   O ambiente de destino talvez não consiga representar todos os intervalos de inteiros.
-   A tradução representa o [**tipo int**](/windows/desktop/WinProg/windows-data-types) da mesma forma que o **tipo long** e [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) da mesma forma que **unsigned long.**
-   O tradutor pode traduzir a constante de caracteres como um conjunto de valores de código diferentes do conjunto para o ambiente de destino. Para determinar as propriedades do ambiente de destino, verifique os valores das macros de LIMITS.H em um aplicativo compilado para o ambiente de destino.
-   A expressão não deve executar consultas ambientais e deve permanecer isolada de detalhes da implementação no computador de destino.

## <a name="examples"></a>Exemplos

Esta seção contém exemplos que demonstram como usar diretivas de pré-processador de compilação condicional.

### <a name="use-of-the-defined-operator"></a>Uso do operador definido

O exemplo a seguir mostra o uso do operador definido. Se o identificador CREDIT for definido, a chamada para a função **de crédito** será compilada. Se o IDENTIFICADOr DEBIT for definido, a chamada para a função **de débito** será compilada. Se nenhum identificador for definido, a chamada para a **função printerror** será compilada. Observe que "CREDIT" e "credit" são identificadores distintos em C e C++ porque seus casos são diferentes.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Uso de \# diretivas if aninhadas

O exemplo a seguir mostra como aninhar \# diretivas if. Este exemplo presume que uma constante simbólica chamada DLEVEL foi definida anteriormente. As \# diretivas elif \# e else são usadas para fazer uma das quatro opções, com base no valor de DLEVEL. A STACK constante é definida como 0, 100 ou 200, dependendo da definição de DLEVEL. Se DLEVEL for maior que 5, STACK não será definido.


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a>Usar para incluir arquivos de header

A compilação condicional é usada normalmente para evitar várias inclusões do mesmo arquivo de cabeçalho. No C++, em que as classes geralmente são definidas em arquivos de título, constructos de compilação condicional podem ser usados para evitar várias definições. O exemplo a seguir determina se a constante simbólica EXAMPLE \_ H está definida. Se sim, o arquivo já foi incluído e não precisa ser reprocessado; caso não seja, a constante EXAMPLE \_ H será definida para indicar esse EXEMPLO. H já foi processado.


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

