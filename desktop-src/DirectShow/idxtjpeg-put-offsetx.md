---
description: O método \_ put OffsetX especifica o deslocamento horizontal da origem do apagaamento.
ms.assetid: 7bc721fd-7e72-49d4-90ae-a193df46326c
title: Método IDxtJpeg::p ut_OffsetX (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3d0e80a847b69d0dd7f0c29eedb751b07baedab2154bb237d2c3e7f816891e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639276"
---
# <a name="idxtjpegput_offsetx-method"></a>Método OffsetX IDxtJpeg::p ut \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_OffsetX` método especifica o deslocamento horizontal da origem do apagando.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_OffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

O deslocamento horizontal da origem do apagando, em pixels. O centro do apagando é deslocada por esse valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDxtJpeg Interface**](idxtjpeg.md)
</dt> </dl>

 

 




