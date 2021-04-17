---
description: Contém o SSID de uma LAN sem fio em formato hexadecimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento Hex (SSID)
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
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762050"
---
# <a name="hex-ssid-element"></a>Elemento Hex (SSID)

O elemento Hex (SSID) contém o SSID de uma LAN sem fio no formato hexadecimal.

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

O elemento é definido pelo elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Comentários

Embora os elementos **hex** e [**Name**](wlan-profileschema-name-ssid-element.md) sejam opcionais, pelo menos um elemento **hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) deve aparecer como um filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Quando as informações de perfil são convertidas em um SSID, o elemento **hex** é convertido para o SSID (se presente) e o elemento [**Name**](wlan-profileschema-name-ssid-element.md) é ignorado. Se o elemento **hex** não estiver presente, o elemento [**Name**](wlan-profileschema-name-ssid-element.md) será convertido em um SSID usando a conversão de Unicode em ASCII.

Quando um SSID é armazenado em um perfil, o elemento **hex** sempre é gerado. O elemento [**Name**](wlan-profileschema-name-ssid-element.md) só será gerado se a conversão de ASCII para Unicode do SSID e a geração do perfil XML forem bem-sucedidas. Algumas informações do SSID original podem ser perdidas quando são convertidas em um [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Exemplos

Para exibir um perfil de exemplo que usa o elemento **hex** , consulte [exemplo de perfil FIPS](fips-profile-sample.md).

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

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




