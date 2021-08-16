---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCRL não foi usado e, portanto, foi liberado em uma chamada subsequente para CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Função de retorno de chamada CertStoreProvFreeFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769931"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Função de retorno de chamada CertStoreProvFreeFindCRL

A função de retorno de chamada **CertStoreProvFreeFindCRL** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) não foi usado e, portanto, é liberado em uma chamada subsequente para **CertStoreProvFindCRL**. Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) devem ser liberados pelo provedor usando **CertStoreProvFindCRL** ou **CertStoreProvFreeFindCRL**.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
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

*pCrlContext* \[ no\]
</dt> <dd>

Um ponteiro para um [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**contexto de CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
