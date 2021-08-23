---
title: Método IMediaRenderer IsAudioSupported
description: Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de áudio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API de streaming de mídia do método IsAudioSupported
- API de streaming de mídia do método IsAudioSupported, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5abe42e65e451464a5f7f3a4d59679db62c3634e95e89e5e275919dd0ece869e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777006"
---
# <a name="imediarendererisaudiosupported-method"></a>Método IMediaRenderer:: IsAudioSupported

Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de áudio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um valor booliano que será **true** se o DMR for capaz de reproduzir o conteúdo de áudio e **false** se não for.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





