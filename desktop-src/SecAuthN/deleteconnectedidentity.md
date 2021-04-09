---
description: Exclui a credencial do usuário usada para a identidade conectada.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Função DeleteConnectedIdentity (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010370"
---
# <a name="deleteconnectedidentity-function"></a>Função DeleteConnectedIdentity

Exclui a credencial do usuário usada para a identidade conectada.

## <a name="syntax"></a>Sintaxe


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProviderHandle* \[ no\]
</dt> <dd>

Identificador do provedor de identidade.

</dd> <dt>

*UserToken* \[ em, opcional\]
</dt> <dd>

Token do usuário conectado cuja conta será convertida em uma conta local. Se *UserToken* não for **NULL**, o provedor de identidade usará esse token para carregar o perfil do usuário e limpar os Estados conectados. Se *UserToken* for **NULL**, o LSA está forçando a desconexão. O provedor de identidade deve limpar todos os Estados conectados globais nesse usuário, mas o provedor não precisa limpar os Estados conectados no perfil do usuário.

</dd> <dt>

*Userid* \[ no\]
</dt> <dd>

O SID principal do usuário conectado. Se *UserToken* não for **NULL**, esse parâmetro será o Sid de usuário do token. Se *UserToken* for **NULL**, esse parâmetro será usado para identificar o usuário conectado e limpar os Estados de conexão global desse usuário.

</dd> <dt>

*IdentityUserName* \[ no\]
</dt> <dd>

O nome de usuário da identidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, a função poderá retornar um dos seguintes códigos de erro.



| Valor retornado                                                                                               | Descrição                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>parâmetro de STATUS \_ inválido \_</dt> </dl>      | Um parâmetro não é válido.<br/>                                                                                                                        |
| <dl> <dt>STATUS \_ não é \_ esse \_ usuário</dt> </dl>          | O usuário identificado por *userid* não existe, não está conectado no momento ou não há nenhuma identidade cujo nome de usuário corresponda a *IdentityUserName*.<br/> |
| <dl> <dt>STATUS de \_ recursos insuficientes \_</dt> </dl> | Não há memória suficiente para processar a solicitação.<br/>                                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Indentitystore. h</dt> </dl> |



 

 




