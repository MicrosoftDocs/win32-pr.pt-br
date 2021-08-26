---
description: O método EffectsEnabled determina se os efeitos estão habilitados. Se os efeitos estão desabilitados, eles permanecem na linha do tempo, mas não são renderizados.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: Método IAMTimeline::EffectsEnabled (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e63561c62f3cbaf7a3a257179167e657ee4d10c6206b6d74062039362b272aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905276"
---
# <a name="iamtimelineeffectsenabled-method"></a>Método IAMTimeline::EffectsEnabled

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EffectsEnabled` método determina se os efeitos estão habilitados. Se os efeitos estão desabilitados, eles permanecem na linha do tempo, mas não são renderizados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Recebe um valor booliana que indica se os efeitos estão habilitados. Se **TRUE**, os efeitos serão habilitados. Se **FALSE**, os efeitos serão desabilitados.

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

 

 




