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
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105784613"
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

## <a name="return-value"></a>Retornar valor

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

 

