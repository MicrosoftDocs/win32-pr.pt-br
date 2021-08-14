---
title: Método IMediaRendererActionInformation IsVolumeAvailable
description: Recupera um valor que indica se o DMR é capaz de ajustar o nível de volume de áudio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API de streaming de mídia do método IsVolumeAvailable
- API de streaming de mídia do método IsVolumeAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce36a9151998a5f7b0a7785aebc1795bd29d31ff47cfdd2368978ad040f3597c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972205"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>Método IMediaRendererActionInformation:: IsVolumeAvailable

Recupera um valor que indica se o DMR é capaz de ajustar o nível de volume de áudio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um valor booliano que será **true** se o DMR for capaz de ajustar o nível de volume de áudio e **false** se não for.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

