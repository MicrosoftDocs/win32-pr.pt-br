---
description: O \_ método Get streams cria uma coleção de fluxos associados ao participante atual.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Método ITParticipant:: get_Streams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766222"
---
# <a name="itparticipantget_streams-method"></a>Método ITParticipant:: get \_ streams

\[**obter \_ Os fluxos** não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ streams** cria uma coleção de fluxos associados ao participante atual. Esse método é fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic. Os aplicativos C e C++ devem usar o método [**EnumerateStreams**](itparticipant-enumeratestreams.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVariant* \[ fora\]
</dt> <dd>

Ponteiro para **Variant** que contém um [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de ponteiros de interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pVariant* não é um ponteiro válido.<br/>     |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) retornada por **ITParticipant:: get \_ streams**. O aplicativo deve chamar **Release** na interface **ITStream** para liberar recursos associados a ela.

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

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

