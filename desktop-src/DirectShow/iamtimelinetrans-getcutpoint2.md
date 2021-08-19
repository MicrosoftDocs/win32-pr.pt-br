---
description: O método GetCutPoint2 recupera o ponto de corte. Esse método é equivalente a IAMTimelineTrans::GetCutPoint, mas aceita um valor REFTIME.
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: Método IAMTimelineTrans::GetCutPoint2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 291aff15260d5d693f3e6b0281d693a7351132fc017358f6f9ee21020dfd4f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952755"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a>Método IAMTimelineTrans::GetCutPoint2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetCutPoint2` método recupera o ponto de corte. Esse método é equivalente a [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), mas aceita um [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTLTime* 
</dt> <dd>

Recebe o ponto de corte, relativo à hora de início da transição, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                               | Descrição                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | O ponto de corte não foi definido. O valor retornado é o valor padrão.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | O ponto de corte foi definido como um valor diferente do padrão.<br/>            |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | Argumento de ponteiro **NULL.**<br/>                                          |



 

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

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




