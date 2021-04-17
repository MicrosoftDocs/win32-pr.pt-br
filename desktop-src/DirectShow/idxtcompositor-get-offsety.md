---
description: O \_ método Get OffsetY recupera o deslocamento vertical do retângulo de destino.
ms.assetid: 78bb3565-7a98-4a64-a2f2-6c34edb47733
title: 'Método IDxtCompositor:: get_OffsetY (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3e8cb2e4552aceb53cf447125ddcc42659d575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779532"
---
# <a name="idxtcompositorget_offsety-method"></a>Método IDxtCompositor:: get \_ OffsetY

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_OffsetY` método recupera o deslocamento vertical do retângulo de destino.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o deslocamento vertical do retângulo de destino, em pixels.

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

[**Interface IDxtCompositor**](idxtcompositor.md)
</dt> </dl>

 

 




