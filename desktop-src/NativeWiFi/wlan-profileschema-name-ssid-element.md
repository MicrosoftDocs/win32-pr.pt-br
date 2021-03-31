---
description: Contém o SSID de uma LAN sem fio.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Elemento Name (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829469"
---
# <a name="name-ssid-element"></a>Elemento Name (SSID)

O elemento Name (SSID) contém o SSID de uma LAN sem fio.

``` syntax
<xs:element name="name">
    <xs:simpleType>
        <xs:restriction
            base="string"
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

Os nomes diferenciam maiúsculas de minúsculas.

Embora os elementos [**hex**](wlan-profileschema-hex-ssid-element.md) e **Name** sejam opcionais, pelo menos um elemento **hex** ou **Name** deve aparecer como um filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Quando as informações de perfil são convertidas em um SSID, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) é convertido para o SSID (se presente) e o elemento **Name** é ignorado. Se o elemento **hex** não estiver presente, o elemento **Name** será convertido em um SSID usando a conversão de Unicode em ASCII.

Quando um SSID é armazenado em um perfil, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) sempre é gerado. O elemento **Name** só será gerado se a conversão de ASCII para Unicode do SSID e a geração do perfil XML forem bem-sucedidas. Algumas informações do SSID original podem ser perdidas quando são convertidas em um **nome**.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Os caracteres de escape XML, como &, não são exibidos. Evite usar caracteres de escape XML em nomes SSID para perfis implantados no Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2.

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **Name** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

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

 

 




