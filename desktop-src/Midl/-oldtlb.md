---
title: comutador/oldtlb
description: A opção/oldtlb instrui o compilador MIDL a gerar uma biblioteca de tipos de formato antigo.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- MIDL do comutador/oldtlb
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b30a7bc905645523a81287eea2dfcdc408b8a4d172cc84282e0f1538e12cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895986"
---
# <a name="oldtlb-switch"></a>comutador/oldtlb

A opção **/oldtlb** instrui o compilador MIDL a gerar uma biblioteca de tipos de formato antigo.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

a opção **/oldtlb** substitui o padrão e direciona o compilador MIDL para gerar bibliotecas de tipo de formato antigo mesmo em versões atuais do Windows usando [createtypelib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) em vez de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Exemplos

**MIDL/oldtlb filename. idl**

**MIDL/oldtlb myoldodl. odl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 