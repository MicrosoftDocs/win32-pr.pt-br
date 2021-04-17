---
description: O \_ método Get Incolocate retorna o tamanho de entrada atual do filtro de redimensionador.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Método IResize:: get_InputSize (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812773"
---
# <a name="iresizeget_inputsize-method"></a>Método IResize:: get \_ Incolocate

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_InputSize` método retorna o tamanho de entrada atual do filtro de redimensionador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piHeight* \[ fora\]
</dt> <dd>

Recebe a altura do vídeo, em pixels.

</dd> <dt>

*piWidth* \[ fora\]
</dt> <dd>

Recebe a largura do vídeo, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o pino de entrada do filtro não estiver conectado, retorne um código de erro. Caso contrário, retorne a largura e a altura do vídeo, conforme especificado pelo tipo de mídia do pino de entrada.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9,0 ou posterior<br/>                                                         |
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IResize**](iresize.md)
</dt> </dl>

 

 




