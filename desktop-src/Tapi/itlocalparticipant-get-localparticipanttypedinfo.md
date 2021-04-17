---
description: O \_ método Get LocalParticipantTypedInfo Obtém informações do participante, como nome de email ou localização geográfica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Método ITLocalParticipant:: get_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779310"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>Método ITLocalParticipant:: get \_ LocalParticipantTypedInfo

O método **Get \_ LocalParticipantTypedInfo** Obtém informações do participante, como nome de email ou localização geográfica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InfoType* \[ no\]
</dt> <dd>

[**Participante \_ do Identificador de \_ informações digitados**](participant-typed-info.md) do tipo de informação necessário.

</dd> <dt>

*ppInfo* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que conterá as informações necessárias após um retorno bem-sucedido do método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O aplicativo deve usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppInfo* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**\_informações de tipo de participante \_**](participant-typed-info.md)
</dt> </dl>

 

