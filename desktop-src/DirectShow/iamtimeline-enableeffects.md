---
description: O método EnableEffects habilita ou desabilita todos os efeitos na linha do tempo. Se os efeitos estão desabilitados, eles permanecem na linha do tempo, mas não são renderizados.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: Método IAMTimeline::EnableEffects (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a6cce5d06b65bb6a7b3b6063e6cf6b9190e268ba7ee5f5abadf4343be2cf64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401107"
---
# <a name="iamtimelineenableeffects-method"></a>Método IAMTimeline::EnableEffects

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EnableEffects` método habilita ou desabilita todos os efeitos na linha do tempo. Se os efeitos estão desabilitados, eles permanecem na linha do tempo, mas não são renderizados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valor booliana que especifica se os efeitos de habilitar ou desabilitar. Se **TRUE**, os efeitos serão habilitados. Se **FALSE**, os efeitos serão desabilitados.

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

[**IAMTimeline Interface**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




