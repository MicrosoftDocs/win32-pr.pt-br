---
description: O método SetCutsOnly especifica se a transição é renderizada como um recorte. Nesse caso, a transição ocorre instantaneamente no ponto de recorte. Se uma transição levar muito tempo para ser renderizada, talvez você queira visualizá-la como uma visualização de velocidade de recortar.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Método IAMTimelineTrans:: SetCutsOnly (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782840"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>Método IAMTimelineTrans:: SetCutsOnly

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetCutsOnly` método especifica se a transição é renderizada como um recorte. Nesse caso, a transição ocorre instantaneamente no ponto de recorte. Se uma transição levar muito tempo para ser renderizada, talvez você queira visualizá-la como uma visualização de velocidade de recortar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Val* 
</dt> <dd>

Especifica se a transição deve ser renderizada como um recorte. Se for **true**, a transição será renderizada como uma recorte instantânea. Se **for false**, a transição renderizará ao longo de sua duração normal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A renderização de uma transição como um recorte não é compatível com a troca de entradas. (Consulte [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) Se você chamar `SetCutsOnly` com um valor de **true**, ele substituirá temporariamente a configuração **SetSwapInputs** . No entanto, a configuração somente de recorte é destinada à visualização, portanto, essa limitação não afeta a saída do arquivo, apenas lembre-se de chamar `SetCutsOnly` com o valor **false** antes de gravar o arquivo.

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

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




