---
description: Recupera uma propriedade especificada de uma CTL (lista de certificados confiáveis).
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
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748396"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Função de retorno de chamada CertStoreProvGetCTLProperty

A função de retorno de chamada **CertStoreProvGetCTLProperty** recupera uma propriedade especificada de uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ).

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

*hStoreProv* \[ no\]
</dt> <dd>

Um identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

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

Um ponteiro para um buffer que contém o ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) a ser retornada pela função. Para obter o valor de *pcbData* antes de alocar memória para o buffer, esse parâmetro pode ser definido como **NULL** em uma primeira chamada para a função.

</dd> <dt>

*pcbData* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará diferente de zero.

Se a função falhar, ela retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**contexto de CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
