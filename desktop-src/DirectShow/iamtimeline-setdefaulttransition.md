---
description: O método SetDefaultTransition define a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: Método IAMTimeline::SetDefaultTransition (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9271e922fe33865feb36b361ae97bb16298b504fb6cbb14066fbd6976c8065e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812406"
---
# <a name="iamtimelinesetdefaulttransition-method"></a>Método IAMTimeline::SetDefaultTransition

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetDefaultTransition` método define a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pguid* 
</dt> <dd>

Ponteiro para uma variável que contém o GUID da transição padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Se você não definir uma transição padrão ou se a transição especificada como padrão causar um erro, o DES usará sua própria transição padrão.

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

[**IAMTimeline Interface**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




