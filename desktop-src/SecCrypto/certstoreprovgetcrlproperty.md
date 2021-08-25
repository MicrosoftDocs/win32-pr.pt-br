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
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877046"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Função de retorno de chamada CertStoreProvGetCRLProperty

A função de retorno de chamada **CertStoreProvGetCRLProperty** recupera uma propriedade especificada de uma [*CRL.*](../secgloss/c-gly.md)

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

*hStoreProv* \[ Em\]
</dt> <dd>

**Alça HCERTSTOREPROV** para um repositório [*de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCrlContext* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura CONTEXT \_ da CRL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)

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

Um ponteiro para um buffer para conter o ponteiro para uma estrutura [**CONTEXT da CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) a ser retornada pela função. Pode ser definido como **NULL** em uma primeira chamada para a função para obter o valor *de pcbData* antes de alocar memória para o buffer.

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

[**CONTEXTO \_ DE CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
