---
description: Esse método retorna um dispositivo associado aos dados de vídeo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Método IVideoFrameNative:: GetDevice'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370649"
---
# <a name="ivideoframenativegetdevice-method"></a>Método IVideoFrameNative:: GetDevice

Esse método retorna um dispositivo associado aos dados de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ no\]
</dt> <dd>

O IID do dispositivo a ser recuperado.

</dd> <dt>

*PPV* \[ fora\]
</dt> <dd>

Quando esse método retorna com êxito, contém o ponteiro do dispositivo solicitado no parâmetro *riid* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK após a conclusão bem-sucedida.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



