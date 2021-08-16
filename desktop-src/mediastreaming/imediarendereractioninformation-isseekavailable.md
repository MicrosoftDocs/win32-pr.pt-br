---
title: Método IsSeekAvailable de IMediaRendererActionInformation
description: Recupera um valor que indica se a DMR está aceitando o método SeekAsync no momento.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API de Streaming de Mídia do método IsSeekAvailable
- API de Streaming de Mídia do método IsSeekAvailable, interface IMediaRendererActionInformation
- API de Streaming de Mídia da interface IMediaRendererActionInformation , método IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b5c7eef78dad4ebfeeebb40c323d7b13e540033eb54852f7da41942f5ec83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735509"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>Método IMediaRendererActionInformation::IsSeekAvailable

Recupera um valor que indica se a DMR está aceitando o [**método SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Um valor boolário que será **True** se a DMR estiver aceitando o método [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) no momento e **False** se não estiver.

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

 

