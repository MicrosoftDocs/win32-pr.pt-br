---
description: Indica se o modo FIPS (Federal Information Processing Standards) está habilitado.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Elemento FIPSmode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647350"
---
# <a name="fipsmode-authencryption-element"></a>Elemento FIPSmode (authEncryption)

O elemento **fipsmode** (authEncryption) indica se o modo FIPS (Federal Information Processing Standards) está habilitado. Quando uma conexão sem fio está operando no modo FIPS, o nível de segurança da conexão é compatível com o padrão FIPS 140-2. Para obter mais informações sobre o FIPS, consulte a [Home Page do FIPS](https://www.itl.nist.gov/fipspubs/).

Esse elemento é opcional. Se esse elemento não for especificado em um perfil, o modo FIPS não estará habilitado.

O **fipsmode** pode ser definido como true somente quando as seguintes condições são atendidas:

-   O elemento [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) tem um valor de `ESS` (ou seja, a conexão é uma conexão de infraestrutura).
-   O elemento de [**autenticação**](wlan-profileschema-authentication-authencryption-element.md) tem um valor de `WPA2` ou `WPA2PSK` .
-   O elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) tem um valor de `AES` .

Ao contrário da maioria dos elementos no esquema de perfil de WLAN \_ , esse elemento está no `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.

O valor do elemento **fipsmode** será ignorado se o driver de Miniport da interface sem fio não oferecer suporte ao modo FIPS.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento. Se **fipsmode** estiver presente em um perfil, o elemento será ignorado.

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Comentários

Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** . Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="examples"></a>Exemplos

Para exibir um perfil de exemplo que usa o elemento **fipsmode** , consulte [exemplo de perfil FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 
