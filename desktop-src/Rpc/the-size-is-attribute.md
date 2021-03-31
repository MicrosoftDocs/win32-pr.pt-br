---
title: O atributo size_is
description: O atributo \ Size \_ is \ está associado a uma constante, expressão ou variável de inteiro que especifica o tamanho de alocação da matriz.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823821"
---
# <a name="the-size_is-attribute"></a>O \[ tamanho \_ é \] atributo

O \[ [atributo \_ size](/windows/desktop/Midl/size-is) é \] associado a uma constante, expressão ou variável de inteiro que especifica o tamanho de alocação da matriz. Considere uma matriz de caracteres cujo comprimento seja determinado pela entrada do usuário:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> O asterisco ( \* ) que marca o espaço reservado para a dimensão da matriz de variável é opcional.

 

O stub do servidor deve alocar memória no servidor que corresponda à memória no cliente para esse parâmetro. A variável que especifica o tamanho deve ser sempre pelo menos um \[ parâmetro [in](/windows/desktop/Midl/in) \] . O atributo direcional é necessário para que o valor de tamanho seja definido na entrada para o stub do servidor. **\[ \]** Esse valor de tamanho fornece informações que o stub de servidor requer para alocar a memória.

O parâmetro Size também pode ser \[ in, [out](/windows/desktop/Midl/out-idl) \] . Isso é útil se, por exemplo, a matriz que o cliente envia não for grande o suficiente para os dados que o servidor precisa armazenar nele. Você pode usar um parâmetro **\[ in, \] out** size para enviar o tamanho necessário de volta para o programa cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vários níveis de ponteiros](multiple-levels-of-pointers.md)
</dt> </dl>

 

 