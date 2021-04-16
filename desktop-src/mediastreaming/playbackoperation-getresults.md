---
title: Método PlaybackOperation. GetResults
description: Retorna os resultados de uma operação assíncrona iniciada por um dos métodos de reprodução MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface PlaybackOperation
- API de streaming de mídia da interface PlaybackOperation, método GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364605"
---
# <a name="playbackoperationgetresults-method"></a>Método PlaybackOperation. GetResults

Retorna os resultados de uma operação assíncrona iniciada por um dos métodos de reprodução [**MediaRenderer**](mediarenderer.md) .

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

O resultado da operação. Um valor de 0 indica que a operação foi concluída. Outros valores são reservados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](playbackoperation-completed.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





