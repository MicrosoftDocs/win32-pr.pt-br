---
description: O método Remove remove esse objeto da linha do tempo (incluindo subobjetos, mas não filhos), para reinserção em outro lugar.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: Método IAMTimelineObj::Remove (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356f7239cbdbe3972f11fcc95dd9bf44dc1b06d086a8e44c9131c0061f3ec211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155259"
---
# <a name="iamtimelineobjremove-method"></a>Método IAMTimelineObj::Remove

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método remove esse objeto da linha do `Remove` tempo (incluindo subobjetos, mas não filhos), para reinserção em outro lugar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Chame esse método somente se o aplicativo inserir imediatamente o objeto de volta na linha do tempo. É uma operação inválida chamar esse método sem reinserir o objeto. Para remover um objeto permanentemente, chame [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).

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

 

 




