---
description: O \_ método Put alfa Especifica o valor alfa para a imagem inteira.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter: método de ut_Alpha de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758838"
---
# <a name="idxtalphasetterput_alpha-method"></a>Método IDxtAlphaSetter::p UT \_ Alpha

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Alpha` método especifica o valor alfa para a imagem inteira.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Alfa* \[ no\]
</dt> <dd>

O valor alfa. Esse valor será aplicado a toda a imagem de destino. Para desabilitar essa propriedade, defina um valor negativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se você definir essa propriedade como um valor não negativo, também deverá desabilitar a propriedade de rampa alfa chamando **Put \_ AlphaRamp** com um valor negativo. Caso contrário, o efeito não será renderizado corretamente.

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

[**IDxtAlphaSetter::p UT \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




