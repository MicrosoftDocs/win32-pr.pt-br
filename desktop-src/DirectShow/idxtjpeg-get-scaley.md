---
description: O \_ método Get ScaleY recupera o valor pelo qual o apagamento é alongado verticalmente.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: 'Método IDxtJpeg:: get_ScaleY (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4ca3feb0177ad1c9172721ca312e810fdb105b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759122"
---
# <a name="idxtjpegget_scaley-method"></a>Método IDxtJpeg:: get \_ ScaleY

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_ScaleY` método recupera a quantidade pela qual o apagamento é alongado verticalmente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o valor pelo qual o apagamento é alongado verticalmente, como uma porcentagem da definição de apagamento original. Por exemplo, o valor 1,0 significa sem alargamento e 2,0 significa 200% de alongamento.

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

 

 




