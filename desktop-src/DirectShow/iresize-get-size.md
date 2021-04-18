---
description: O \_ método obter tamanho retorna o tamanho de saída atual e o modo de ampliação.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Método IResize:: get_Size (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759071"
---
# <a name="iresizeget_size-method"></a>Método de tamanho IResize:: get \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Size` método retorna o tamanho de saída atual e o modo de ampliação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
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

</dd> <dt>

*pFlag* \[ fora\]
</dt> <dd>

Recebe um sinalizador que especifica o modo de ampliação. Consulte [**redimensionar sinalizadores**](resize-flags.md) para obter os valores possíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o tipo de saída não tiver sido definido, o filtro deverá retornar valores padrão. Esses valores podem ser escolhidos arbitrariamente em tempo de design.

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

 

 




