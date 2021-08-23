---
description: O método get \_ Participants cria uma coleção de participantes associados à conferência atual.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: Método ITParticipantControl::get_Participants (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d61d12de18e30bd86d42fd1aa75aed2048c42e487e019eabe3da6d65e70a9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864707"
---
# <a name="itparticipantcontrolget_participants-method"></a>Método ITParticipantControl::get \_ Participants

\[**get \_ Os participantes** não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método get \_ Participants** cria uma coleção de participantes associados à conferência atual. Esse método é fornecido para aplicativos cliente de Automação, como aqueles escritos em Visual Basic. Os aplicativos C e C++ devem usar o [**método EnumerateParticipants.**](itparticipantcontrol-enumerateparticipants.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVariant* \[ out\]
</dt> <dd>

Ponteiro para **VARIANT** que contém [**uma ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de ponteiros de interface [**ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro pVariant* não é um ponteiro válido.<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

TAPI chama o **método AddRef** na interface [**ITParticipant**](itparticipant.md) retornada por **ITParticipantControl::get \_ Participants**. O aplicativo deve chamar **Release** na interface **ITParticipant** para liberar recursos associados a ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




