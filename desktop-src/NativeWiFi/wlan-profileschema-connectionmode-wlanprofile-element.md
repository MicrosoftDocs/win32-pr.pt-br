---
description: Indica se a conexão com uma LAN sem fio deve ser automática ou iniciada pelo usuário.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento ConnectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647713"
---
# <a name="connectionmode-wlanprofile-element"></a>Elemento ConnectionMode (WLANProfile)

O elemento ConnectionMode (WLANProfile) indica se a conexão com uma LAN sem fio deve ser automática ou iniciada pelo usuário.

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como ESS, esse valor poderá ser automático ou manual. O valor padrão será auto se esse elemento estiver ausente.

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como IBSS, esse valor deverá ser manual.

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **ConnectionMode** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Comentários

A tabela a seguir descreve os valores de enumeração.



| Valor  | Descrição                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | A conexão com a rede sem fio deve ser iniciada automaticamente sempre que a rede estiver no intervalo. |
| manual | A conexão com a rede sem fio só é iniciada peloda mediante a solicitação explícita de um usuário.               |



 

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **ConnectionMode** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




