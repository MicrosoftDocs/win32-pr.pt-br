---
description: Função proxy para o método SetColorContexts.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: IWICBitmapFrameEncode_SetColorContexts_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8f939c3ea5836c152e65f1fe0f5aff5ccf5941e1811691a41a6d8f44bc8ade3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812376"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a>Função proxy IWICBitmapFrameEncode \_ SetColorContexts \_

Função proxy para o [**método SetColorContexts.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Ponteiro para este [**objeto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)

</dd> <dt>

*cCount* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O número de perfis [**IWICColorContext a**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) definir.

</dd> <dt>

*ppIColorContext* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Um ponteiro para um [**ponteiro IWICColorContext que**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) contém os perfis de contextos de cor a definir para o quadro.

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



 

 




