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
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811289"
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

*hStoreProv* \[ no\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*dwPropId* \[ no\]
</dt> <dd>

Indica um identificador de propriedade.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*pvData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que contém o ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) a ser retornada pela função. Pode ser definido como **NULL** em uma primeira chamada para a função para obter o valor de *pcbData* antes de alocar memória para o buffer.

</dd> <dt>

*pcbData* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData* .

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
</dt> </dl>

 

 
