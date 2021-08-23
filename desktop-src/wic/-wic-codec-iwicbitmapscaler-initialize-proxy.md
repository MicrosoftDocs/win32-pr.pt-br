---
description: IWICBitmapScaler_Initialize_Proxy função - função proxy para o método Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be9fee37147ff3fcadf1ea13f566aab3d34faf00d7a3c7f126af7b401d7af538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965315"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a>Função Inicializar Proxy IWICBitmapScaler \_ \_

Função proxy para o [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***

Ponteiro para este [**objeto IWICBitmapScaler.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)

</dd> <dt>

*pISource* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

A origem do bitmap de entrada.

</dd> <dt>

*uiWidth* \[ Em\]
</dt> <dd>

Tipo: **UINT**

A largura de destino.

</dd> <dt>

*uiHeight* \[ Em\]
</dt> <dd>

Tipo: **UINT**

A altura da desinização.

</dd> <dt>

*modo* \[ Em\]
</dt> <dd>

Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**

O modo de interpolação a ser usado ao dimensionar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, Windows aplicativos da área de trabalho do Vista \[\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




