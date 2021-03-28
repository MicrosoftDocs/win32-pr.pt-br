---
title: " Diretivas If, elif, Else e endif"
description: Diretivas de pré-processador que controlam a compilação de partes de um arquivo de origem.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Diretivas If, elif, Else e endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084553"
---
# <a name="if-elif-else-and-endif-directives"></a>\#Diretivas If, \# elif, \# else e \# endif

Diretivas de pré-processador que controlam a compilação de partes de um arquivo de origem.



| \#Se *ifCondition* ...         |
|--------------------------------|
| \[\#*elifCondition* de elif...\] |
| \[\#senão...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condição principal a ser avaliada. Se esse parâmetro for avaliado como um valor diferente de zero, todo o texto entre essa \# diretiva If e a próxima instância da \# diretiva elif, \# Else ou \# endif será mantido na unidade de tradução; caso contrário, o código-fonte subsequente não será retido. <br/> A condição pode usar o operador de pré-processador definido para determinar se uma macro ou constante de pré-processador específico está definida; Esse uso é equivalente ao uso da diretiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Consulte a seção comentários para obter restrições sobre o valor do parâmetro *ifCondition* . <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ adicional\] <br/> | Outra condição a ser avaliada. Se o parâmetro *ifCondition* e todas as \# diretivas elif anteriores forem avaliadas como zero, e esse parâmetro for avaliado como um valor diferente de zero, todo o texto entre essa \# diretiva elif e a próxima instância da \# diretiva elif, \# Else ou \# endif será mantido na unidade de tradução; caso contrário, o código-fonte subsequente não será retido. <br/> A condição pode usar o operador de pré-processador definido para determinar se uma macro ou constante de pré-processador específico está definida; Esse uso é equivalente ao uso da diretiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Consulte a seção comentários para obter restrições sobre o valor do parâmetro *elifCondition* . <br/> |



 

## <a name="remarks"></a>Comentários

Cada \# diretiva If em um arquivo de origem deve ser correspondida por uma \# diretiva de fechamento endif. Qualquer número de \# diretivas de elif pode aparecer entre as \# diretivas If e \# endif, mas no máximo uma \# diretiva else é permitida. A \# diretiva Else, se presente, deve ser a última diretiva antes de \# endif. As diretivas de compilação condicional contidas nos arquivos de inclusão devem atender às mesmas condições.

As \# diretivas If, \# elif, \# else e \# endif podem aninhar as partes de texto de outras \# diretivas If. Cada diretiva aninhada \# Else, \# elif ou \# endif pertence à diretiva precedentes mais próxima \# .

Se nenhuma condição for avaliada como um valor diferente de zero, o pré-processador selecionará o bloco de texto após a \# diretiva else. Se a \# cláusula else for omitida e nenhuma condição for avaliada como um valor diferente de zero, nenhum bloco de texto será selecionado.

Os parâmetros *ifCondition* e *elifCondition* muito atendem aos seguintes requisitos:

-   As expressões de compilação condicional são tratadas como valores [**longos assinados**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) e essas expressões são avaliadas usando as mesmas regras que as expressões em C++.
-   As expressões devem ter o tipo integral e podem incluir apenas constantes de inteiros, constantes de caracteres e o operador defined.
-   As expressões não podem usar **sizeof** ou um operador de conversão de tipo.
-   O ambiente de destino talvez não consiga representar todos os intervalos de inteiros.
-   A conversão representa o tipo [**int**](/windows/desktop/WinProg/windows-data-types) , o mesmo que o tipo **Long**, e o [**int não assinado**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) é o mesmo que o **Long não assinado**.
-   O tradutor pode traduzir a constante de caracteres como um conjunto de valores de código diferentes do conjunto para o ambiente de destino. Para determinar as propriedades do ambiente de destino, verifique os valores das macros de LIMITS.H em um aplicativo compilado para o ambiente de destino.
-   A expressão não deve executar consultas ambientais e deve permanecer isolada de detalhes da implementação no computador de destino.

## <a name="examples"></a>Exemplos

Esta seção contém exemplos que demonstram como usar as diretivas de pré-processador de compilação condicional.

### <a name="use-of-the-defined-operator"></a>Uso do operador definido

O exemplo a seguir mostra o uso do operador definido. Se o crédito do identificador for definido, a chamada para a função de **crédito** será compilada. Se o débito do identificador for definido, a chamada para a função **Debit** será compilada. Se nenhum identificador for definido, a chamada para a função de **erro** é compilada. Observe que "crédito" e "crédito" são identificadores distintos em C e C++ porque seus casos são diferentes.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Uso de \# diretivas If aninhadas

O exemplo a seguir mostra como aninhar as \# diretivas If. Este exemplo supõe que uma constante simbólica denominada DLEVEL tenha sido definida anteriormente. As \# diretivas elif e \# else são usadas para fazer uma das quatro opções, com base no valor de DLEVEL. A pilha de constantes é definida como 0, 100 ou 200, dependendo da definição de DLEVEL. Se DLEVEL for maior que 5, STACK não será definido.


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



### <a name="use-for-including-header-files"></a>Usar para incluir arquivos de cabeçalho

A compilação condicional é usada normalmente para evitar várias inclusões do mesmo arquivo de cabeçalho. Em C++, em que as classes geralmente são definidas em arquivos de cabeçalho, as construções de compilação condicional podem ser usadas para impedir várias definições. O exemplo a seguir determina se o exemplo de constante simbólico \_ H está definido. Nesse caso, o arquivo já foi incluído e não precisa ser reprocessado; caso contrário, o exemplo de constante \_ H é definido para indicar esse exemplo. H já foi processada.


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

 

