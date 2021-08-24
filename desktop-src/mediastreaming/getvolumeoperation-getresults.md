---
title: Método GetVolumeOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetVolumeOperation
- API de streaming de mídia da interface GetVolumeOperation, método GetResults
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e58188a0d8b0d2ed13a9cb7d7486f440f4a1303ca32208371690965f976339d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011846"
---
# <a name="getvolumeoperationgetresults-method"></a>Método GetVolumeOperation. GetResults

Retorna os resultados da operação assíncrona iniciada pelo [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

O volume. Um valor entre 0 e 100. 0 indica o volume mínimo e 100 indica o volume máximo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](getvolumeoperation-completed.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

