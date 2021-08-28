---
title: Método IsImageSupported de IMediaRenderer
description: Recupera um valor que indica se a DMR é capaz de exibir imagens.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API de Streaming de Mídia do método IsImageSupported
- API de Streaming de Mídia do método IsImageSupported, interface IMediaRenderer
- API de Streaming de Mídia da interface IMediaRenderer, método IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fae20b6b5486586e305723a1d6a29a885bf0db8b8741ab9e6881fb292f35d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461636"
---
# <a name="imediarendererisimagesupported-method"></a>Método IMediaRenderer::IsImageSupported

Recupera um valor que indica se a DMR é capaz de exibir imagens.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Um valor booliana que **será True se** a DMR for capaz de exibir imagens e **False** se não for.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





