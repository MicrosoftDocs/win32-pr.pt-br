---
description: Indica se a autenticação 802.1 X é usada.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Elemento useOneX (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759190"
---
# <a name="useonex-authencryption-element"></a>Elemento useOneX (authEncryption)

O elemento useOneX (authEncryption) indica se a autenticação 802.1 X é usada.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **useOneX** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**authEncryption (segurança)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




