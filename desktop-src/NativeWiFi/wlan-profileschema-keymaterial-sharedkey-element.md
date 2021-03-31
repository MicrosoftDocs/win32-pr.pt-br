---
description: Contém uma chave de rede ou frase secreta.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Elemento keymaterial (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169709"
---
# <a name="keymaterial-sharedkey-element"></a>Elemento keymaterial (sharedKey)

O elemento keymaterial (sharedKey) contém uma chave de rede ou frase secreta. Se o elemento [**protegido**](wlan-profileschema-protected-sharedkey-element.md) tiver um valor de true, esse material da chave será criptografado; caso contrário, o material da chave será descriptografado. O material de chave criptografado é expresso em formato hexadecimal.

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

O elemento é definido pelo elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Comentários

O intervalo de valores válidos para o elemento keymaterial varia de acordo com o tipo de autenticação e criptografia usado, conforme especificado pelos elementos de [**autenticação**](wlan-profileschema-authentication-authencryption-element.md) e [**criptografia**](wlan-profileschema-encryption-authencryption-element.md) . Ele também varia por [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).

A tabela a seguir mostra valores de **keymaterial** válidos para alguns pares de autenticação e criptografia.



| valor de [**autenticação**](wlan-profileschema-authentication-authencryption-element.md) | valor de [**criptografia**](wlan-profileschema-encryption-authencryption-element.md) | valor [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) | Valores de **Keymaterial** válidos                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| aberto ou compartilhado                                                                           | WEP                                                                              | networkKey                                                            | Esse elemento contém uma chave WEP de 5 ou 13 caracteres ANSI, ou de 10 ou 26 caracteres hexadecimais.                                                                                             |
| WPAPSK ou WPA2PSK                                                                        | TKIP ou AES                                                                      | Senha                                                            | Esse elemento contém uma frase secreta de 8 a 63 caracteres ASCII, ou seja, de 8 a 63 caracteres ANSI no intervalo de 32 a 126. Os valores de chave devem estar em conformidade com os requisitos especificados pelo 802.11 i. |
| WPAPSK ou WPA2PSK                                                                        | TKIP ou AES                                                                      | networkKey                                                            | Esse elemento contém uma chave de 64 caracteres hexadecimais.                                                                                                                                      |



 

Caracteres Unicode podem ser inseridos onde os caracteres ANSI ou ASCII são especificados acima. No entanto, se os caracteres Unicode fornecidos não puderem ser mapeados para caracteres ANSI ou ASCII, o material de chave fornecido será rejeitado.

O material da chave retornado pelo [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) é sempre criptografado. Além disso, se o material de chave não criptografado for passado para [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), o material da chave será criptografado automaticamente antes de ser armazenado no repositório de perfis.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O material da chave nunca é criptografado.

Se o processo for executado no contexto da conta LocalSystem, você poderá descriptografar o material da chave chamando [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **keymaterial** , consulte exemplo de [perfil sem difusão](non-broadcast-profile-sample.md), [exemplo de perfil WPA-Pessoal](wpa-personal-profile-sample.md)e [exemplo de perfil WPA2-Pessoal](wpa2-personal-profile-sample.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**sharedKey (segurança)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
