---
description: Uma função definida pelo aplicativo que cria uma lista de SIDs (identificadores de segurança) que se aplicam a um cliente. AuthzComputeGroupsCallback é um espaço reservado para o nome da função definida pelo aplicativo.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Função de retorno de chamada AuthzComputeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663598"
---
# <a name="authzcomputegroupscallback-callback-function"></a>Função de retorno de chamada AuthzComputeGroupsCallback

A função **AuthzComputeGroupsCallback** é uma função definida pelo aplicativo que cria uma lista de SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) que se aplicam a um cliente. **AuthzComputeGroupsCallback** é um espaço reservado para o nome da função definida pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hAuthzClientContext* \[ no\]
</dt> <dd>

Um identificador para um contexto de cliente.

</dd> <dt>

*Argumentos* \[ no\]
</dt> <dd>

Dados passados no parâmetro *DynamicGroupArgs* de uma chamada para a função [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)ou [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .

</dd> <dt>

*pSidAttrArray* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável de ponteiro que recebe o endereço de uma matriz de [**Sid e estruturas de \_ \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Essas estruturas representam os grupos aos quais o cliente pertence.

</dd> <dt>

*pSidCount* \[ fora\]
</dt> <dd>

O número de estruturas em *pSidAttrArray*.

</dd> <dt>

*pRestrictedSidAttrArray* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável de ponteiro que recebe o endereço de uma matriz de [**Sid e estruturas de \_ \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Essas estruturas representam os grupos dos quais o cliente é restrito.

</dd> <dt>

*pRestrictedSidCount* \[ fora\]
</dt> <dd>

O número de estruturas em *pSidRestrictedAttrArray*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função retornar com êxito uma lista de SIDs, o valor de retorno será **true**.

Se a função falhar, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Os aplicativos também podem adicionar SIDs ao contexto do cliente chamando [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).

As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                   |
| Redistribuível<br/>          | Pacote de ferramentas de administração do Windows Server 2003 no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções básicas de controle de acesso](authorization-functions.md)
</dt> <dt>

[**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ e \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

