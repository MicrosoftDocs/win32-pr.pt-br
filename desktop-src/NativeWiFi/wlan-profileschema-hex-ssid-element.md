---
description: Contém o SSID de uma LAN sem fio em formato hexadecimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento hex (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 666562f7a476505dbb0ff23d5354e0f073505d9dd5195bcae17543294cc5f176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799886"
---
# <a name="hex-ssid-element"></a>Elemento hex (SSID)

O elemento hexadecimal (SSID) contém o SSID de uma LAN sem fio em formato hexadecimal.

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

## <a name="remarks"></a>Comentários

Embora os **elementos hexa e** [**name**](wlan-profileschema-name-ssid-element.md) sejam opcionais, pelo menos um elemento **hexa** ou [**nome**](wlan-profileschema-name-ssid-element.md) deve aparecer como um filho do [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

Quando as informações de perfil são convertidas em um SSID, o elemento **hex** é convertido no SSID (se presente) e o [**elemento name**](wlan-profileschema-name-ssid-element.md) é ignorado. Se o **elemento hexaxa** não estiver presente, o elemento [**name**](wlan-profileschema-name-ssid-element.md) será convertido em um SSID usando Unicode para conversão ASCII.

Quando um SSID é armazenado em um perfil, o **elemento hexaxa** é sempre gerado. O [**elemento**](wlan-profileschema-name-ssid-element.md) name só será gerado se a conversão ASCII em Unicode do SSID e a geração de perfil XML for bem-sucedida. Algumas informações do SSID original podem ser perdidas quando são convertidas em um [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Exemplos

Para exibir um perfil de exemplo que usa o **elemento hexa,** consulte [Exemplo de perfil FIPS](fips-profile-sample.md).

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

[**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




