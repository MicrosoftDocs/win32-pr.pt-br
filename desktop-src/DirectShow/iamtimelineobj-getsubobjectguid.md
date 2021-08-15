---
description: O método GetSubObjectGUID recupera o GUID do subobjeto associado a esse objeto de linha do tempo.
ms.assetid: c2787e6b-ed72-4a6c-9e1e-c79c00020585
title: Método IAMTimelineObj::GetSubObjectGUID (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a1afa22c2a850ce0f6106fcb8ffe1d82a84338fa03354e073e2c114678363d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400754"
---
# <a name="iamtimelineobjgetsubobjectguid-method"></a>Método IAMTimelineObj::GetSubObjectGUID

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSubObjectGUID` método recupera o GUID do subobjeto associado a este objeto de linha do tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSubObjectGUID(
   GUID *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pval* 
</dt> <dd>

Receberá o GUID do subobjeto ou GUID NULL se \_ o objeto não tiver um subobjeto.

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

[**IAMTimelineObj Interface**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




