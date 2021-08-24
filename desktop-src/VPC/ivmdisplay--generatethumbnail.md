---
title: Método de _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual. | Método de _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail o método virtual PC
- _GenerateThumbnail método virtual PC, interface IVMDisplay
- IVMDisplay interface virtual PC, método de _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5decd1b3c55ab6513408a81eb37d422fac495334fb545c4cad4806050a8af7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654366"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>Método IVMDisplay:: \_ GenerateThumbnail

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*thumbnailImage* \[ fora\]
</dt> <dd>

A matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface retorna a miniatura com mais eficiência do que a propriedade [**thumbnail**](ivmdisplay-thumbnail.md) , mas não pode ser usada por clientes de script. A miniatura tem sempre 64 pixels de largura por 48 pixels de altura. Cada pixel é 32 bits, em que os 8 bits superiores representam o valor azul do pixel, os próximos 8 bits representam o valor verde do pixel e os próximos 8 bits representam o valor vermelho do pixel. Os primeiros 64 elementos na matriz são a primeira linha da miniatura, os próximos 64 elementos são a segunda linha e assim por diante. Esse método retorna uma matriz estática de pixels, que é mais eficiente do que retornar um **SafeArray** de valores **variantes** , mas não é compatível com clientes de script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

