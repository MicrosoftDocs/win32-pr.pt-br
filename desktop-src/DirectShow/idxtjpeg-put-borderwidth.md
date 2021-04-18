---
description: O método de Put \_ BorderWidth especifica a largura da borda sólida ao longo das bordas do padrão de apagamento.
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: 'IDxtJpeg: método de ut_BorderWidth de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df7435b8a516b818b6d7c86e907ba75cce86f6c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759119"
---
# <a name="idxtjpegput_borderwidth-method"></a>Método IDxtJpeg::p UT \_ BorderWidth

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_BorderWidth` método especifica a largura da borda sólida ao longo das bordas do padrão de apagamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

A largura da borda, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

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
</dt> </dl>

 

 




