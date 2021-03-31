---
description: Esse método retorna uma interface que fornece acesso aos dados de vídeo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Método IVideoFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920914"
---
# <a name="ivideoframenativegetdata-method"></a>Método IVideoFrameNative:: GetData

Esse método retorna uma interface que fornece acesso aos dados de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ no\]
</dt> <dd>

O IID da interface a ser recuperada.

</dd> <dt>

*PPV* \[ fora\]
</dt> <dd>

Quando esse método retorna com êxito, contém o ponteiro de interface solicitado no parâmetro *riid* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK após a conclusão bem-sucedida. Retorna E \_ nointerface se a interface solicitada não puder ser encontrada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



