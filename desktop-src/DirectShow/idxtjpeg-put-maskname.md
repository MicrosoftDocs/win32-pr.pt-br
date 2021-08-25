---
description: O método \_ put MaskName especifica o nome de um arquivo JPEG a ser usado como a máscara de apagador.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: Método IDxtJpeg::p ut_MaskName (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7a43398020c49f2a6dab1cd56fc0244c4be88e2e45e38e0f6bd63c119bbf66a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755936"
---
# <a name="idxtjpegput_maskname-method"></a>Método MaskName IDxtJpeg::p ut \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_MaskName` método especifica o nome de um arquivo JPEG a ser usado como a máscara de apagando. Essa máscara será usada em vez de uma das máscaras de apagar. O arquivo deve conter um gradiente monocromático de 8 bits por pixel. O gradiente é usado como uma máscara para definir a progressão do apagamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

Especifica o nome do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Para reverter para uma máscara criada, de definir a **propriedade MaskNum.**

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
</dt> <dt>

[**IDxtJpeg::put \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




