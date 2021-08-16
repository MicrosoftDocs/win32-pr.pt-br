---
title: Método setnotify IAMWMBufferPass
description: O método setnotificate é usado por aplicativos para fornecer o filtro de leitura ASF do WM ou do leitor ASF do WM com um ponteiro para a interface IAMWMBufferPassCallback do aplicativo.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Método setnotify Windows Media Format
- Método setnotify Windows Media Format, interface IAMWMBufferPass
- IAMWMBufferPass interface Windows Media Format, método setnotificate
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47e189a2654ed4c760fdfcd6ced5506cc90d5e7cc989a7f79979e6d95b0bbfb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847602"
---
# <a name="iamwmbufferpasssetnotify-method"></a>Método IAMWMBufferPass:: setnotificar

O método **Setnotificate** é usado por aplicativos para fornecer o filtro de leitura ASF do WM ou do [leitor ASF do WM](wm-asf-reader-filter.md) com um ponteiro para a interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCallback* \[ no\]
</dt> <dd>

Ponteiro para a interface **IAMWMBufferPassCallback** do aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Chame esse método antes de colocar o gráfico de filtro no estado de execução.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 