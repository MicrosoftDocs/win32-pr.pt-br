---
title: Métodos ID2D1Factory CreateWicBitmapRenderTarget
description: Cria um destino de renderização que renderiza para um bitmap do WIC (Microsoft Windows Imaging Component).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Métodos CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 177f5459d8245292e2962e502882bb86643f3f8b777efd8a336fde5f8c671897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698176"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>Métodos ID2D1Factory::CreateWicBitmapRenderTarget

Cria um destino de renderização que renderiza para um bitmap do WIC (Microsoft Windows Imaging Component).

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                            | Descrição                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET PROPERTIES , \_ \_ \* ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Cria um destino de renderização que renderiza para um bitmap do WIC (Microsoft Windows Imaging Component).<br/> |
| [**CreateWicBitmapRenderTarget(IWICBitmap,D2D1 \* \_ RENDER TARGET PROPERTIES \_ \_&,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Cria um destino de renderização que renderiza para um bitmap do WIC (Microsoft Windows Imaging Component).<br/> |



## <a name="remarks"></a>Comentários

Seu aplicativo deve criar destinos de renderização uma vez e mantê-los por toda a vida útil do aplicativo ou até que o erro [**D2DERR \_ RECREATE \_ TARGET**](direct2d-error-codes.md) seja recebido. Ao receber esse erro, você precisará recriar o destino de renderização (e todos os recursos que ele criou).

**Observação**   Esse método não tem suporte no Windows Phone e falhará quando chamado em um dispositivo com código de erro 0x8899000b ( Não há nenhum dispositivo de renderização de hardware disponível para esta operação ). Como o Windows Phone Emulator dá suporte à renderização WARP, esse método falhará quando chamado no emulador com um código de erro diferente, 0x88982f80 (wincodec \_ err \_ unsupportedpixelformat).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

