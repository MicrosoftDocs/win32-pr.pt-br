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
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993766"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK após a conclusão bem-sucedida. Retorna E \_ nointerface se a interface solicitada não puder ser encontrada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



