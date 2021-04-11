---
description: A função AuthzFreeCentralAccessPolicyCallback é uma função definida pelo aplicativo que libera a memória alocada pela função AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Função de retorno de chamada AuthzFreeCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172322"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Função de retorno de chamada AuthzFreeCentralAccessPolicyCallback

A função *AuthzFreeCentralAccessPolicyCallback* é uma função definida pelo aplicativo que libera a memória alocada pela função [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) . *AuthzFreeCentralAccessPolicyCallback* é um espaço reservado para o nome da função definida pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCentralAccessPolicy* \[ no\]
</dt> <dd>

Ponteiro para a política de acesso central a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará **true**.

Se a função não puder executar a avaliação, ela retornará **false**. Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de todas as AUTHZ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
