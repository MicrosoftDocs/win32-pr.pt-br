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
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750194"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Função de retorno de chamada AuthzGetCentralAccessPolicyCallback

A função *AuthzGetCentralAccessPolicyCallback* é uma função definida pelo aplicativo que recupera a política de acesso central. *AuthzGetCentralAccessPolicyCallback* é um espaço reservado para o nome da função definida pelo aplicativo.

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

*hAuthzClientContext* \[ no\]
</dt> <dd>

Identificador para o contexto do cliente.

</dd> <dt>

*capid* \[ no\]
</dt> <dd>

ID da política de acesso central a ser recuperada.

</dd> <dt>

*pArgs* \[ em, opcional\]
</dt> <dd>

Argumentos opcionais que foram passados para a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) por meio do membro **OptionalArguments** da estrutura de [**solicitação de \_ acesso \_ do AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ fora\]
</dt> <dd>

Ponteiro para um valor booliano que o Gerenciador de recursos usa para indicar se uma política de acesso central deve ser usada durante a avaliação do acesso.

</dd> <dt>

*ppCentralAccessPolicy* \[ fora\]
</dt> <dd>

Ponteiro para a política de acesso central (CAP) a ser usado para avaliar o acesso. Se esse valor for **NULL**, a extremidade padrão será aplicada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará **true**.

Se a função não puder executar a avaliação, ela retornará **false**. Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                   |
| Redistribuível<br/>          | Pacote de ferramentas de administração do Windows Server 2003 no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_solicitação de acesso de AUTHZ \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**informações de todas as AUTHZ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

