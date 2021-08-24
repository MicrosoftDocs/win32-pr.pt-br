---
description: Indica se a conexão com uma LAN sem fio deve ser automática ou iniciada pelo usuário.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento connectionMode (WLANProfile)
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
ms.openlocfilehash: a6ef18eff8ba27a3169399f1f10e0707c4e0b3c010d54830ad8f8f997c5e1b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684435"
---
# <a name="connectionmode-wlanprofile-element"></a>Elemento connectionMode (WLANProfile)

O elemento connectionMode (WLANProfile) indica se a conexão com uma LAN sem fio deve ser automática ou iniciada pelo usuário.

Se [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como ESS, esse valor poderá ser automático ou manual. O valor padrão será automático se esse elemento estiver ausente.

Se [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como IBSS, esse valor deverá ser manual.

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

O **elemento connectionMode** é definido pelo [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="remarks"></a>Comentários

A tabela a seguir descreve os valores de enumeração.



| Valor  | Descrição                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | A conexão com a rede sem fio deve ser iniciada automaticamente sempre que a rede estiver no intervalo. |
| manual | A conexão com a rede sem fio é initada somente mediante a solicitação explícita de um usuário.               |



 

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o **elemento connectionMode,** consulte [Exemplos de perfil sem fio.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                |
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

 

 




