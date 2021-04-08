---
description: A estrutura UpdateEndpointProxySettings define as configurações de proxy usadas ao solicitar um token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Estrutura UpdateEndpointProxySettings (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010541"
---
# <a name="updateendpointproxysettings-structure"></a>Estrutura UpdateEndpointProxySettings

A estrutura **UpdateEndpointProxySettings** define as configurações de proxy usadas ao solicitar um token.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a>Membros

<dl> <dt>

**szProxyAddr**
</dt> <dd>

O nome DNS ou o endereço IP do servidor proxy a ser usado (por exemplo, "proxy.somecorp.com" ou "192.168.0.4") ou uma cadeia de caracteres vazia se não for necessário usar nenhum proxy.

</dd> <dt>

**szBypassList**
</dt> <dd>

Uma lista de endereços de host que devem ignorar o servidor proxy ou uma cadeia de caracteres vazia se todos os endereços de host tiverem que usar o servidor proxy

O WUA não usará esses dados se **szProxyAddr** estiver vazio.

</dd> <dt>

**szUserName**
</dt> <dd>

O nome de usuário que é usado para autenticar com o servidor proxy ou a cadeia de caracteres vazia se nenhuma autenticação for necessária.

O WUA não usará esses dados se **szProxyAddr** estiver vazio.

</dd> <dt>

**szPassword**
</dt> <dd>

A senha usada para autenticar com o servidor proxy ou a cadeia de caracteres vazia se nenhuma autenticação for necessária.

O WUA não usará esses dados se **szProxyAddr** estiver vazio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                              |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




