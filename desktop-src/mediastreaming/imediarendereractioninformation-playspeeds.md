---
title: Método IMediaRendererActionInformation PlaySpeeds
description: Recupera a lista completa de valores PlaySpeed que são aceitos pelo DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API de streaming de mídia do método PlaySpeeds
- API de streaming de mídia do método PlaySpeeds, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294010"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>IMediaRendererActionInformation: método laySpeeds de:P

Recupera a lista completa de valores [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que são aceitos pelo DMR.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um vetor de estruturas [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) especificando a lista completa de valores de **PlaySpeed** que são aceitos pelo DMR.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

