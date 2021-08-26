---
title: Método StreamSelectOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo SelectBestStreamAsync.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface StreamSelectOperation
- API de streaming de mídia da interface StreamSelectOperation, método GetResults
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 022e75a57b9b38cff2a1e477d78a164767ab8cbcd4e1d3a159e8f61c8972fb95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952476"
---
# <a name="streamselectoperationgetresults-method"></a>Método StreamSelectOperation. GetResults

Retorna os resultados da operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

