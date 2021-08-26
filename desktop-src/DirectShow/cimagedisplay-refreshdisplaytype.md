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
ms.openlocfilehash: d9184d5e8a0e0ad6c0242ec1dc4b7590f1bc0d39a0a9cd6a09b2676563a2796e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055466"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se for bem-sucedido ou E \_ falhar se não for bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método inicializa o membro de **\_ exibição m** para um tipo de vídeo que corresponde ao modo de exibição no dispositivo especificado.

Chame esse método sempre que uma \_ mensagem do WM DISplaychanged for recebida ou para especificar um dispositivo de vídeo secundário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




