---
description: O \_ método Put mascaraname especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg: método de ut_MaskName de:p (QEdit. h)'
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
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757675"
---
# <a name="idxtjpegput_maskname-method"></a>Método IDxtJpeg::p UT \_ maskname

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_MaskName` método especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento. Essa máscara será usada em vez de uma das máscaras de apagamento internas. O arquivo deve conter um gradiente monocromático de 8 bits por pixel. O gradiente é usado como uma máscara para definir a progressão do apagamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

Especifica o nome do arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Para reverter para uma máscara interna, defina a propriedade **MaskNum** .

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IDxtJpeg**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg::p UT \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




