---
description: Recupera uma propriedade especificada de um certificado.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Função de retorno de chamada CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c7d338c94c4e9655c125b0f70e3f2e8dfa732316a970c74c26e4a7fbced22671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769921"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Função de retorno de chamada CertStoreProvGetCertProperty

A função de retorno de chamada **CertStoreProvGetCertProperty** recupera uma propriedade especificada de um certificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
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

Um ponteiro para uma [**estrutura CONTEXT \_ CERT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*dwPropId* \[ Em\]
</dt> <dd>

Indica um identificador de propriedade.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*pvData* \[ out\]
</dt> <dd>

Um ponteiro para um buffer para conter o ponteiro para uma [**estrutura CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) a ser retornada pela função. Pode ser definido como **NULL** em uma primeira chamada para a função para obter o valor *de pcbData* antes de alocar memória para o buffer.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData.*

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
</dt> </dl>

 

 
