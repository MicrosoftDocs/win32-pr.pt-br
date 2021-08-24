---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCert não foi usado e, portanto, liberado, em uma chamada subsequente para CertStoreProvFindCert.
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
ms.openlocfilehash: ab2a6ae1bd8199e7bed97626c83241223fc3943b94fcb387868331329d8740a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877296"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Função de retorno de chamada CertStoreProvFreeFindCert

A função de retorno de chamada **CertStoreProvFreeFindCert** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) não foi usado e, portanto, liberado, em uma chamada subsequente para **CertStoreProvFindCert.** Antes que o retorno de chamada CLOSE seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) devem ser liberados pelo provedor usando **CertStoreProvFindCert** ou **CertStoreProvFreeFindCert**.

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

*hStoreProv* \[ Em\]
</dt> <dd>

**Alça HCERTSTOREPROV** para um repositório [*de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ Em\]
</dt> <dd>

Um ponteiro para um [**CONTEXTO \_ DE CERTIFICADO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*pvStoreProvFindInfo* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer que contém informações de encontre.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a função for bem-sucedida **ou FALSE** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONTEXTO DO \_ CERTIFICADO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
