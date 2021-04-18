---
description: Define o tipo de tokens que podem ser usados para autenticação com um ponto de extremidade.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumeração UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788731"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Enumeração UpdateEndpointAuthTokenType

Define o tipo de tokens que podem ser usados para autenticação com um ponto de extremidade.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**
</dt> <dd>

Nenhum token de autenticação é necessário.

</dd> <dt>

<span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**
</dt> <dd>

O token de autenticação para o ponto de extremidade é um token WS-Security SAML (Security Assertion Markup Language) 1,1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                              |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




