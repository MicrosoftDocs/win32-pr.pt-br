---
description: Especifica a origem das configurações de segurança 802.1 X usadas por um componente de segurança do IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Elemento useMSOneX (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4a62f2f25ef2a4a52fae82e2ce8ddb097a4b434d7c2f8f35a2783703a617ad8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912636"
---
# <a name="usemsonex-ihv-element"></a>Elemento useMSOneX (IHV)

O elemento **useMSOneX** (IHV) especifica a origem das configurações de segurança 802.1 x usadas por um componente de segurança do IHV.

Quando **useMSOneX** é verdadeiro, os componentes de segurança de IHV usam configurações 802.1 x definidas pela Microsoft. Quando **useMSOneX** é false, os componentes de segurança de IHV usam configurações 802.1 x fornecidas pelo fornecedor.

**Windows xp com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

O elemento é definido pelo elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




