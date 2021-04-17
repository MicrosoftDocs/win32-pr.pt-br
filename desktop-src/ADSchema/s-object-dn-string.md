---
title: Sintaxe de objeto (DN-String)
description: Uma cadeia de caracteres de octeto que contém um valor de cadeia de caracteres e um DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de objeto (DN-String) do AD
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769092"
---
# <a name="objectdn-string-syntax"></a>Sintaxe de objeto (DN-String)

Uma cadeia de caracteres de octeto que contém um valor de cadeia de caracteres e um DN.



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Objeto (DN-String)                                                                  |
| ID da sintaxe    | 2.5.5.14                                                                           |
| ID DO OM        | 127                                                                                |
| Tipo de MAPI    | \-                                                                                 |
| Tipo de ADS     | \_DN ADSTYPE \_ com \_ cadeia de caracteres                                                          |
| Tipo de variante | expedição de VT \_                                                                       |
| Tipo SDS     | Um objeto COM que pode ser convertido em um [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Comentários

Um valor com essa sintaxe tem o seguinte formato:

``` syntax
S:<char count>:<string value>:<object DN>
```

onde " &lt; contagem &gt; de caracteres" é o número de caracteres na cadeia de caracteres "valor da cadeia de caracteres &lt; &gt; " e " &lt; DN &gt; do objeto" é um nome distinto de um objeto em Active Directory. Active Directory atualizará o DN se o objeto ao qual ele se refere for movido ou renomeado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
