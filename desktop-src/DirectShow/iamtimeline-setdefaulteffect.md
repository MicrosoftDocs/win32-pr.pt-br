---
description: O método SetDefaultEffect define o efeito padrão. Se o mecanismo de renderização não puder renderizar um efeito, ele substituirá o efeito padrão.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: Método IAMTimeline::SetDefaultEffect (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 43eb0dcb51b80b1cc6e59f9e864f9f80fd32a381c04602a7c7ce9733683fca3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052836"
---
# <a name="iamtimelinesetdefaulteffect-method"></a>Método IAMTimeline::SetDefaultEffect

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetDefaultEffect` método define o efeito padrão. Se o mecanismo de renderização não puder renderizar um efeito, ele substituirá o efeito padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pguid* 
</dt> <dd>

Ponteiro para o GUID do efeito padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Se você não definir um efeito padrão ou se o efeito especificado como padrão causar um erro, o DES usará seu próprio efeito padrão.

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

 

 




