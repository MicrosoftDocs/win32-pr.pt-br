---
title: Método IMediaRenderer IsVideoSupported
description: Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de vídeo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API de streaming de mídia do método IsVideoSupported
- API de streaming de mídia do método IsVideoSupported, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293346"
---
# <a name="imediarendererisvideosupported-method"></a>Método IMediaRenderer:: IsVideoSupported

Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um valor booliano que será **true** se o DMR for capaz de reproduzir conteúdo de vídeo e **false** se não for.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





