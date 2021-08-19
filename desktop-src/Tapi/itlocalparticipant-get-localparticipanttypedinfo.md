---
description: O método get LocalParticipantTypedInfo obtém informações do participante, como o nome do email ou \_ a localização geográfica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: Método ITLocalParticipant::get_LocalParticipantTypedInfo (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41afb4c55ba769e341b81e5ec1ca721745509ba8bf2bdfd88ae22ebc48bb535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003364"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>Método ITLocalParticipant::get \_ LocalParticipantTypedInfo

O **método \_ get LocalParticipantTypedInfo** obtém informações do participante, como o nome do email ou a localização geográfica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InfoType* \[ Em\]
</dt> <dd>

[**PARTICIPANTE \_ Identificador \_ DE INFORMAÇÕES**](participant-typed-info.md) TYPED do tipo de informação necessária.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Ponteiro para um **BSTR** que conterá as informações necessárias após um retorno bem-sucedido do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O aplicativo deve usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o *parâmetro ppInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**INFORMAÇÕES \_ DIGITADOS DO \_ PARTICIPANTE**](participant-typed-info.md)
</dt> </dl>

 

