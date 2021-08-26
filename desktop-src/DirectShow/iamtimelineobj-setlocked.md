---
description: O método SetLocked define o estado de edição do objeto como bloqueado ou desbloqueado.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: Método IAMTimelineObj::SetLocked (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 87298b4e1fe9bc821c72d46d09d55e898b453292940029b7189a92e455b4c206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052476"
---
# <a name="iamtimelineobjsetlocked-method"></a>Método IAMTimelineObj::SetLocked

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetLocked` método define o estado de edição do objeto como bloqueado ou desbloqueado.

Um estado bloqueado indica que o objeto não deve ser editado; um estado desbloqueado indica que o objeto pode ser editado. A linha do tempo não impõe o bloqueio. A configuração bloqueada existe apenas para conveniência do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* 
</dt> <dd>

Valor booliana que especifica o estado de edição do objeto. Se **TRUE**, o objeto será bloqueado e não deverá ser editado. Se **FALSE**, o objeto será desbloqueado e poderá ser editado.

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

 

 




