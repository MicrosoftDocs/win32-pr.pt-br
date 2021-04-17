---
description: O método MakeIdentityPalette tenta tornar uma paleta de \# identidade &0034;, &\# 0034; definida como uma que é mapeada diretamente para a paleta selecionada no dispositivo de vídeo.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Método CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748445"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>Método CImagePalette. MakeIdentityPalette

O `MakeIdentityPalette` método tenta criar uma "paleta de identidade", definida como uma que é mapeada diretamente para a paleta selecionada no dispositivo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pEntry* 
</dt> <dd>

Ponteiro para uma matriz de entradas de paleta.

</dd> <dt>

*iColours* 
</dt> <dd>

Número de entradas de paleta em *pentry*.

</dd> <dt>

*szDevice* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI. Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido ou S \_ false se for malsucedido.

## <a name="remarks"></a>Comentários

Esse método compara as entradas reservadas na paleta do sistema com as entradas correspondentes na matriz *pentry* . Se eles corresponderem exatamente, o método definirá o \_ sinalizador de DESrecolhimento do PC nas entradas de paleta restantes (não reservadas) em *pentry*. Esse sinalizador impede que o GDI tente mapear entradas de paleta lógica para entradas da paleta do sistema.

O método [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




