---
description: Uma função definida pelo aplicativo que manipula ACEs (entradas de controle de acesso) de retorno de chamada durante uma verificação de acesso.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Função de retorno de chamada AuthzAccessCheckCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5079b740d268174715b6c944787bb687cd9b8b1ecb12a27c04eeb26c79811034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784152"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Função de retorno de chamada AuthzAccessCheckCallback

A função **AuthzAccessCheckCallback** é uma função definida pelo aplicativo que manipula ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) de retorno de chamada durante uma verificação de acesso. **AuthzAccessCheckCallback** é um espaço reservado para o nome da função definida pelo aplicativo. O aplicativo registra esse retorno de chamada chamando [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hAuthzClientContext* \[ no\]
</dt> <dd>

Um identificador para um contexto de cliente.

</dd> <dt>

*ritmo* \[ no\]
</dt> <dd>

Um ponteiro para a ACE a ser avaliada para inclusão na chamada à função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

</dd> <dt>

*pArgs* \[ em, opcional\]
</dt> <dd>

Dados passados no parâmetro *DynamicGroupArgs* da chamada para [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) ou [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).

</dd> <dt>

*pbAceApplicable* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma variável booliana que recebe os resultados da avaliação da lógica definida pelo aplicativo.

Os resultados serão **verdadeiros** se a lógica determinar que a ACE é aplicável e será incluída na chamada para [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); caso contrário, os resultados serão **falsos**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, a função retornará **true**.

Se a função não puder executar a avaliação, ela retornará **false**. Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.

## <a name="remarks"></a>Comentários

As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional, caso contrário, o termo de expressão condicional que as referenciará será avaliado como desconhecido.

Para obter mais informações, consulte as visões gerais [sobre como o AccessCheck funciona](how-dacls-control-access-to-an-object.md) e a [política de autorização centralizada](centralized-authorization-policy.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                   |
| Redistribuível<br/>          | Windows pacote de ferramentas de administração do Server 2003 no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções básicas de controle de acesso](authorization-functions.md)
</dt> <dt>

[Política de autorização centralizada](centralized-authorization-policy.md)
</dt> <dt>

[Como a AccessCheck funciona](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

