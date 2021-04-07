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
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828006"
---
# <a name="certstoreprovdeletectl-callback-function"></a>Função de retorno de chamada CertStoreProvDeleteCTL

A função de retorno de chamada **CertStoreProvDeleteCTL** é chamada por [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) antes de excluir uma CTL da loja. Essa função determina se uma CTL pode ser excluída.

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

*hStoreProv* \[ no\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se uma CTL puder ser excluída do repositório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



 

 
