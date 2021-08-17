---
title: Método IMediaRendererActionInformation IsMuteAvailable
description: Recupera um valor que indica se a DMR é capaz de muting do áudio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API de Streaming de Mídia do método IsMuteAvailable
- API de Streaming de Mídia do método IsMuteAvailable, interface IMediaRendererActionInformation
- API de Streaming de Mídia da interface IMediaRendererActionInformation , método IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 331e2831ff18656f23a3d7067b8ab472835bf4a25760f6e86a92302621048a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871063"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>Método IMediaRendererActionInformation::IsMuteAvailable

Recupera um valor que indica se a DMR é capaz de muting do áudio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Um valor boolano que será **True** se a DMR for capaz de muting o áudio e **False** se não for.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

