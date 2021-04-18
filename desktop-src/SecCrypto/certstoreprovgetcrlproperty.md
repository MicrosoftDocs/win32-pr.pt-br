---
description: Recupera uma propriedade especificada de uma CRL.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Função de retorno de chamada CertStoreProvGetCRLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760391"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Função de retorno de chamada CertStoreProvGetCRLProperty

A função de retorno de chamada **CertStoreProvGetCRLProperty** recupera uma propriedade especificada de uma [*CRL*](../secgloss/c-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
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

*pCrlContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .

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

Um ponteiro para um buffer que contém o ponteiro para uma estrutura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) a ser retornada pela função. Pode ser definido como **NULL** em uma primeira chamada para a função para obter o valor de *pcbData* antes de alocar memória para o buffer.

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

[**contexto de CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
