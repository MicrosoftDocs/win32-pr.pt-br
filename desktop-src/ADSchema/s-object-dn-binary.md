---
title: Sintaxe de objeto (DN-binário)
description: Uma cadeia de caracteres de octeto que contém um valor binário e um DN (nome distinto).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de objeto (DN binário) do AD
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086563"
---
# <a name="objectdn-binary-syntax"></a>Sintaxe de objeto (DN-binário)

Uma cadeia de caracteres de octeto que contém um valor binário e um DN (nome distinto).



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Objeto (DN-binário)                                                                  |
| ID da sintaxe    | 2.5.5.7                                                                            |
| ID DO OM        | 127                                                                                |
| Tipo de MAPI    | TSTRING                                                                            |
| Tipo de ADS     | \_DN ADSTYPE \_ com \_ binário                                                          |
| Tipo de variante | expedição de VT \_                                                                       |
| Tipo SDS     | Um objeto COM que pode ser convertido em um [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Comentários

Um valor com essa sintaxe tem o seguinte formato:

``` syntax
B:<char count>:<binary value>:<object DN>
```

onde " &lt; contagem &gt; de caracteres" é o número de dígitos hexadecimais em " &lt; valor binário &gt; ", " &lt; valor binário &gt; " é a representação HEXADECIMAL do valor binário e "DN do &lt; objeto &gt; " é um nome diferenciado. Active Directory atualizará automaticamente o DN se o objeto ao qual ele se refere for movido ou renomeado. Para obter mais informações e um exemplo de código que usa essa sintaxe, consulte [habilitando a associação de renomeação segura com a propriedade otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
