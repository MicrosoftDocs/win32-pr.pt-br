---
description: Especifica o método de autenticação a ser usado para se conectar à LAN sem fio.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Elemento Authentication (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164872"
---
# <a name="authentication-authencryption-element"></a>Elemento Authentication (authEncryption)

O elemento Authentication (authEncryption) especifica o método de autenticação a ser usado para conectar-se à LAN sem fio.

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Comentários

A tabela a seguir descreve os valores de enumeração.



| Valor   | Descrição                            |
|---------|----------------------------------------|
| Abrir    | Abra a autenticação 802,11.            |
| shared  | Autenticação compartilhada 802,11.          |
| WPA     | WPA-Enterprise a autenticação 802,11.  |
| WPAPSK  | WPA-Personal a autenticação 802,11.    |
| WPA2    | WPA2-Enterprise a autenticação 802,11. |
| WPA2PSK | WPA2-Personal a autenticação 802,11.   |



 

Para obter mais informações sobre os métodos de autenticação 802,11, consulte as especificações de [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento de **autenticação** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

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

 

 




