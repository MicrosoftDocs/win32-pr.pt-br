---
title: opção/ms_union
description: A \_ opção Union/MS controla o alinhamento de NDR de uniões não encapsuladas. Observe que esse atributo é fornecido para compatibilidade com versões anteriores.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union MIDL do comutador
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823334"
---
# <a name="ms_union-switch"></a>\_opção de União/MS

A **opção \_ Union/MS** controla o alinhamento de NDR de uniões não encapsuladas.

> [!Note]  
> Esse atributo é fornecido para compatibilidade com versões anteriores. Não é recomendável para uso em uma nova interface.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

O compilador MIDL espelha o comportamento do compilador de IDL uso-DCE para uniões não encapsuladas. No entanto, como as versões anteriores do compilador MIDL não faziam isso, a opção **\_ Union/MS** fornece compatibilidade com interfaces criadas em versões anteriores do compilador MIDL.

O \_ recurso de União MS pode ser usado como uma opção de linha de comando (**/MS \_ Union**), um atributo de interface IDL ou como um atributo de tipo IDL.

## <a name="examples"></a>Exemplos

**arquivo de \_ União MIDL/MS. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




