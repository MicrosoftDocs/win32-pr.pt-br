---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCert não foi usado e, portanto, foi liberado em uma chamada subsequente para CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Função de retorno de chamada CertStoreProvFreeFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755956"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Função de retorno de chamada CertStoreProvFreeFindCert

A função de retorno de chamada **CertStoreProvFreeFindCert** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) não foi usado e, portanto, é liberado em uma chamada subsequente para **CertStoreProvFindCert**. Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) devem ser liberados pelo provedor usando **CertStoreProvFindCert** ou **CertStoreProvFreeFindCert**.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
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

*pCertContext* \[ no\]
</dt> <dd>

Um ponteiro para um [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

</dd> <dt>

*pvStoreProvFindInfo* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém informações de localização.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a função for bem-sucedida ou **false** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**contexto do certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
