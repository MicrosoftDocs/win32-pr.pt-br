---
title: Método GetResults GetTransportInformationOperation
description: Retorna os resultados da operação assíncrona iniciada pelo GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetTransportInformationOperation
- API de streaming de mídia da interface GetTransportInformationOperation, método GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbcc6345a09d0553df240c57e50b4498618be76cc75814f268892aa6e0b4dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100630"
---
# <a name="gettransportinformationoperationgetresults-method"></a>Método GetTransportInformationOperation:: GetResults

Retorna os resultados da operação assíncrona iniciada pelo [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

Uma referência a uma estrutura [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) que contém os resultados da operação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](gettransportinformationoperation-completed.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

