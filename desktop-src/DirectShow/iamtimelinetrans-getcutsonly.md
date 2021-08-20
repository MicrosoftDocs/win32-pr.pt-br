---
description: O método GetCutsOnly determina se a transição é renderizada como um corte. Nesse caso, a transição ocorre instantaneamente no ponto de corte.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: Método IAMTimelineTrans::GetCutsOnly (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7007db4699dc3f1772ad727c2e40daa15946d07d564b92b5b1517899ff6e1f20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154780"
---
# <a name="iamtimelinetransgetcutsonly-method"></a>Método IAMTimelineTrans::GetCutsOnly

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetCutsOnly` método determina se a transição é renderizada como um corte. Nesse caso, a transição ocorre instantaneamente no ponto de corte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pval* 
</dt> <dd>

Recebe um valor booliana que especifica se a transição é renderizada como um corte. Se **TRUE**, a transição será um corte instantâneo. Se **FALSE**, a transição ocorrerá durante sua duração normal.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

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

[**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




