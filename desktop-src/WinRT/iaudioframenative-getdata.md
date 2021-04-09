---
description: Esse método retorna uma interface que fornece acesso aos dados de áudio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Método IAudioFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090415"
---
# <a name="iaudioframenativegetdata-method"></a>Método IAudioFrameNative:: GetData

Esse método retorna uma interface que fornece acesso aos dados de áudio.

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

Tipo: **REFIID**

O IID da interface a ser recuperada.

</dd> <dt>

*PPV* \[ fora\]
</dt> <dd>

Tipo: **LPVOID \** _

Quando esse método retorna com êxito, contém o ponteiro de interface solicitado no parâmetro _riid *.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna S \_ OK após a conclusão bem-sucedida. Retorna E \_ nointerface se a interface solicitada não puder ser encontrada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



