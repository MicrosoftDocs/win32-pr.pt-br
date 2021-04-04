---
title: Método Notify IAMWMBufferPassCallback
description: O método Notify é chamado pelo PIN para cada buffer que é entregue durante o streaming.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Método Notify Windows Media Format
- Método Notify Windows Media Format, interface IAMWMBufferPassCallback
- IAMWMBufferPassCallback interface formato Windows Media, método Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084795"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>Método IAMWMBufferPassCallback:: Notify

O método **Notify** é chamado pelo PIN para cada buffer que é entregue durante o streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNSSBuffer3* \[ no\]
</dt> <dd>

Ponteiro para a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) exposta no exemplo de mídia.

</dd> <dt>

*pPin* \[ no\]
</dt> <dd>

Ponteiro para o PIN associado ao fluxo de mídia ao qual o exemplo pertence.

</dd> <dt>

*prtStart* \[ no\]
</dt> <dd>

Hora de início do exemplo.

</dd> <dt>

*prtEnd* \[ no\]
</dt> <dd>

Hora de término do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum valor de retorno específico foi especificado. O PIN de chamada ignora o **HRESULT**.

## <a name="remarks"></a>Comentários

Esse método permite que um aplicativo examine e atue em informações no buffer de mídia antes que o conteúdo do buffer seja processado. O aplicativo é responsável por saber o tipo de mídia no PIN. Essas informações podem ser obtidas primeiro obtendo as informações de fluxo do perfil e, em seguida, chamando o método [**IConfigAsfWriter2:: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) para determinar qual PIN está associado a cada fluxo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência do QASF do DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Interface IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interface INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 