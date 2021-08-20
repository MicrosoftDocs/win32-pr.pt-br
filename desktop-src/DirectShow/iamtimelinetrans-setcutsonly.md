---
description: O método SetCutsOnly especifica se a transição é renderizada como um corte. Nesse caso, a transição ocorre instantaneamente no ponto de corte. Se uma transição levar muito tempo para renderizar, talvez você queira visualiza-la como uma versão prévia de recortar para velocidade.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: Método IAMTimelineTrans::SetCutsOnly (Qedit.h)
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
ms.openlocfilehash: 3b008e0aef31548dcba71f3b2a2940009c0cd0c71786bd9bd733c206c1d68ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154719"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>Método IAMTimelineTrans::SetCutsOnly

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetCutsOnly` método especifica se a transição é renderizada como um corte. Nesse caso, a transição ocorre instantaneamente no ponto de corte. Se uma transição levar muito tempo para renderizar, talvez você queira visualiza-la como uma versão prévia de recortar para velocidade.

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

Especifica se a transição deve ser renderização como um corte. Se **TRUE**, a transição será renderizada como um corte instantâneo. Se **FALSE**, a transição será renderizada durante sua duração normal.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Renderizar uma transição como um corte não é compatível com a troca das entradas. (Consulte [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) Se você chamar `SetCutsOnly` com um valor **TRUE,** ele substituirá temporariamente a **configuração SetSwapInputs.** No entanto, a configuração somente de reduções destina-se à visualização, portanto, essa limitação não afeta a saída do arquivo. Lembre-se apenas de chamar com o valor FALSE antes de `SetCutsOnly` escrever o arquivo. 

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

[**IAMTimelineTrans Interface**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




