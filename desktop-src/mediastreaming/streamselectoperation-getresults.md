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
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105815478"
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

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

