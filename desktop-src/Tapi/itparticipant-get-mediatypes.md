---
description: O \_ método Get MediaTypes Obtém os tipos de mídia associados a um participante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Método ITParticipant:: get_MediaTypes (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811927"
---
# <a name="itparticipantget_mediatypes-method"></a>Método ITParticipant:: obter \_ MediaTypes

\[**obter \_ As MediaTypes** não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ MediaTypes** Obtém os [**tipos de mídia**](tapimediatype--constants.md) associados a um participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plMediaType* \[ fora\]
</dt> <dd>

Ponteiro para sinalizadores de tipo de mídia, como \_ vídeo TAPIMEDIATYPE.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *plMediaType* não é um ponteiro válido.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**tipos de mídia**](tapimediatype--constants.md)
</dt> </dl>

 

 




