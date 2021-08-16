---
description: Uma função definida pelo aplicativo que libera a memória alocada pela função AuthzComputeGroupsCallback. AuthzFreeGroupsCallback é um espaço reservado para o nome da função definida pelo aplicativo.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Função de retorno de chamada AuthzFreeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3cce78e261892fede79fb8fc76bc5b0d009342db3e0bf672be2854cb8492bcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783760"
---
# <a name="authzfreegroupscallback-callback-function"></a>Função de retorno de chamada AuthzFreeGroupsCallback

A **função AuthzFreeGroupsCallback** é uma função definida pelo aplicativo que libera a memória alocada pela [**função AuthzComputeGroupsCallback.**](authzcomputegroupscallback.md) **AuthzFreeGroupsCallback** é um espaço reservado para o nome da função definida pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSidAttrArray* \[ Em\]
</dt> <dd>

Um ponteiro para a memória alocada por [**AuthzComputeGroupsCallback.**](authzcomputegroupscallback.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função de retorno de chamada não retorna um valor.

## <a name="remarks"></a>Comentários

As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                   |
| Redistribuível<br/>          | Windows Pacote de Ferramentas de Administração do Server 2003 no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções básicas de controle de acesso](authorization-functions.md)
</dt> <dt>

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




