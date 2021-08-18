---
description: A função AuthzGetCentralAccessPolicyCallback é uma função definida pelo aplicativo que recupera a política de acesso central. AuthzGetCentralAccessPolicyCallback é um espaço reservado para o nome da função definida pelo aplicativo.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Função de retorno de chamada AuthzGetCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5e8fd0afbd901d48386859e9b5d3557a173cfe6a23d749dc776992a4aedebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783740"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Função de retorno de chamada AuthzGetCentralAccessPolicyCallback

A *função AuthzGetCentralAccessPolicyCallback* é uma função definida pelo aplicativo que recupera a política de acesso central. *AuthzGetCentralAccessPolicyCallback* é um espaço reservado para o nome da função definida pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hAuthzClientContext* \[ Em\]
</dt> <dd>

Lidar com o contexto do cliente.

</dd> <dt>

*capid* \[ Em\]
</dt> <dd>

ID da política de acesso central a ser recuperada.

</dd> <dt>

*pArgs* \[ in, opcional\]
</dt> <dd>

Argumentos opcionais que foram passados para a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) por meio do membro **OptionalArguments** da estrutura [**AUTHZ \_ ACCESS \_ REQUEST.**](/windows/desktop/api/Authz/ns-authz-authz_access_request)

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ out\]
</dt> <dd>

Ponteiro para um valor booliana que o gerenciador de recursos usa para indicar se uma política de acesso central deve ser usada durante a avaliação de acesso.

</dd> <dt>

*ppCentralAccessPolicy* \[ out\]
</dt> <dd>

Ponteiro para a CAP (política de acesso central) a ser usada para avaliar o acesso. Se esse valor for **NULL,** o CAP padrão será aplicado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função **retornará TRUE.**

Se a função não puder executar a avaliação, ela retornará **FALSE.** Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                   |
| Redistribuível<br/>          | Windows Pacote de Ferramentas de Administração do Server 2003 no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SOLICITAÇÃO DE \_ ACESSO \_ AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**INFORMAÇÕES DE \_ INIT DO AUTHZ \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

