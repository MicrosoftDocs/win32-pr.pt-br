---
description: Chamado por CertDeleteCTLFromStore antes de excluir uma CTL do repositório.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Função de retorno de chamada CertStoreProvDeleteCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: befc031c1be441ad23c7a50563030775b625b81b66a9e1f92df4fb7c641fe73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993086"
---
# <a name="certstoreprovdeletectl-callback-function"></a>Função de retorno de chamada CertStoreProvDeleteCTL

A função de retorno de chamada **CertStoreProvDeleteCTL** é chamada por [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) antes de excluir uma CTL do repositório. Essa função determina se uma CTL pode ser excluída.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hStoreProv* \[ Em\]
</dt> <dd>

**Alça HCERTSTOREPROV** para um repositório [*de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**CTL \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se uma CTL puder ser excluída do armazenamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



 

 
