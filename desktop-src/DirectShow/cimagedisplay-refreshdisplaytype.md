---
description: O método RefreshDisplayType atualiza o formato de vídeo do objeto para corresponder à exibição especificada.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Método CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759319"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>Método CImageDisplay. RefreshDisplayType

O `RefreshDisplayType` método atualiza o formato de vídeo do objeto para corresponder à exibição especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szDeviceName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI. Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou E \_ falhar se não for bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método inicializa o membro de **\_ exibição m** para um tipo de vídeo que corresponde ao modo de exibição no dispositivo especificado.

Chame esse método sempre que uma \_ mensagem do WM DISplaychanged for recebida ou para especificar um dispositivo de vídeo secundário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




