---
description: Uma função de retorno de chamada usada para notificar o host quando um carregamento de textura for concluído.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5Callbacks:: LoadTextureFromFileComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763977"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>Método IPixEngine5Callbacks:: LoadTextureFromFileComplete

Uma função de retorno de chamada usada para notificar o host quando um carregamento de textura for concluído.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a>Parâmetros

*textureid*   
A ID da textura carregada.

*textureDesc*   
O descritor de textura da textura carregada.

*numSlices*   
O número de fatias que a textura tem.

*Count2 \_ sliceIndicies*   
As índicos de fatia associadas à textura.

*Count2 \_ sliceDescriptors*   
Descritores para cada fatia.

*numFormatOverrides*   
O número de substituições de formato.

*count5 \_ formatOverrides*   
O formato substitui.

*histograma*   
O endereço dos dados de histograma para a textura carregada.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
