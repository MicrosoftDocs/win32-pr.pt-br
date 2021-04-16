---
description: O \_ método Put AlphaRamp especifica a propriedade de rampa alfa. A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados. Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter: método de ut_AlphaRamp de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758056"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>IDxtAlphaSetter: método UT \_ AlphaRamp:p

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_AlphaRamp` método especifica a propriedade de rampa alfa. A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados. Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Alfa* \[ no\]
</dt> <dd>

A rampa alfa como uma porcentagem. Por exemplo, 1,0 é 100%. Para desabilitar essa propriedade, defina um valor negativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se você definir essa propriedade como um valor não negativo, também deverá desabilitar a propriedade Alpha chamando **Put \_ alfa** com um valor negativo. Caso contrário, o efeito não será renderizado corretamente.

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

[**Interface IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::p UT \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




