---
title: Método notify IAMWMBufferPassCallback
description: O método Notify é chamado pelo pin para cada buffer que é entregue durante o streaming.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Formato de mídia do windows do método Notify
- Notificar formato de mídia do windows do método , interface IAMWMBufferPassCallback
- Formato de mídia da interface IAMWMBufferPassCallback , método Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847531"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>Método IAMWMBufferPassCallback::Notify

O **método Notify** é chamado pelo pin para cada buffer que é entregue durante o streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNSSBuffer3* \[ Em\]
</dt> <dd>

Ponteiro para a interface [**INSSBuffer3 exposta**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) no exemplo de mídia.

</dd> <dt>

*pPin* \[ Em\]
</dt> <dd>

Ponteiro para o pino associado ao fluxo de mídia ao que o exemplo pertence.

</dd> <dt>

*prtStart* \[ Em\]
</dt> <dd>

Hora de início do exemplo.

</dd> <dt>

*prtEnd* \[ Em\]
</dt> <dd>

Hora de término do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum valor de retorno específico é especificado. O pino de chamada ignora o **HRESULT.**

## <a name="remarks"></a>Comentários

Esse método permite que um aplicativo examine e atue em informações no buffer de mídia antes que o conteúdo do buffer seja processado. O aplicativo é responsável por conhecer o tipo de mídia no pino. Essas informações podem ser obtidas primeiro obtendo as informações de fluxo do perfil e, em seguida, chamando o método [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) para determinar qual pino está associado a cada fluxo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DirectShow Referência de QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**IAMWMBufferPassCallback Interface**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**INSSBuffer3 Interface**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 