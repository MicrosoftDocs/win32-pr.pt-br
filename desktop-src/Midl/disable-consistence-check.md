---
title: disable_consistency_check atributo
description: Direciona o RPC para não impor a verificação de consistência de correlação.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291951"
---
# <a name="disable_consistency_check-attribute"></a>desabilitar \_ o \_ atributo de verificação de consistência

Direciona o RPC para não impor a verificação de consistência de correlação.

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

Para parâmetros correlacionados, o RPC irá impor que um buffer não nulo seja passado quando a variável de contagem de correlação for não nula.

## <a name="example"></a>Exemplo

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

Se *MyString* for **NULL**, o RPC rejeitará a chamada, a menos que Length esteja definido como 0. Observe que o RPC permitirá que o *comprimento* seja 0 enquanto o *MYSTRING* não for nulo e o RPC tratará *MyString* como uma alocação de buffer de comprimento 0.

## <a name="remarks"></a>Comentários

Para desabilitar essa verificação, a IDL pode conter o \[ \_ atributo Desabilitar verificação de consistência \_ \] em um tipo de parâmetro, typedef ou ponteiro. Isso direcionará o RPC para não impor a consistência entre o ponteiro do buffer e a variável de correlação para o buffer apontado pelo parâmetro ou ponteiro.

Para desabilitar a verificação de consistência de uma compilação de MIDL inteira (e desabilitar a imposição da verificação em todos os casos), a opção de linha de comando MIDL [/Backward \_ compatível com maybenull \_ tamanho](-backward-compat.md) pode ser usada. Isso exige que o destino da compilação MIDL seja pelo menos â € "Target NT60.

 

 




