---
description: Recupera uma propriedade especificada de uma CTL (lista de confiança de certificado).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Função de retorno de chamada CertStoreProvGetCTLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1677c2cccbdf0b422696437736380bd0bb57542220a898332d72ec7a0562fd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769755"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Função de retorno de chamada CertStoreProvGetCTLProperty

A função de retorno de chamada **CertStoreProvGetCTLProperty** recupera uma propriedade especificada de uma CTL (lista de confiança [*de*](../secgloss/c-gly.md) certificado).

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

Um **alça HCERTSTOREPROV para** um repositório de [*certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**CTL \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)

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

Um ponteiro para um buffer para conter o ponteiro para uma [**estrutura CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) a ser retornada pela função. Para obter o valor *de pcbData* antes de alocar memória para o buffer, esse parâmetro pode ser definido como **NULL** em uma primeira chamada para a função.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará diferentes de zero.

Se a função falhar, ela retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONTEXTO DE \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
