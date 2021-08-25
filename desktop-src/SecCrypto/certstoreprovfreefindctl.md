---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCTL não foi usado e, portanto, foi liberado em uma chamada subsequente para CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Função de retorno de chamada CertStoreProvFreeFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5f3f6d224ed19073408015b3b83b90a66e9402d9b838d50eb7a8381e312e0534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877136"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Função de retorno de chamada CertStoreProvFreeFindCTL

A função de retorno de chamada **CertStoreProvFreeFindCTL** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) não foi usado e, portanto, é liberado em uma chamada subsequente para **CertStoreProvFindCTL**. Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) devem ser liberados pelo provedor usando **CertStoreProvFindCTL** ou **CertStoreProvFreeFindCTL**.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
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

Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*pvStoreProvFindInfo* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém informações de localização.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a função for bem-sucedida ou **false** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**contexto de CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
