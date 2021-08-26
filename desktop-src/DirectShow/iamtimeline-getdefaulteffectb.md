---
description: O método GetDefaultEffectB recupera o efeito padrão. Esse método é equivalente a IAMTimeline::GetDefaultEffect, mas recebe um valor BSTR em vez de um GUID.
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: Método IAMTimeline::GetDefaultEffectB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f0abfac297817b4e93b4eabe5bd2517c22ab363498bbbe35f2b5ae449524ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997766"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>Método IAMTimeline::GetDefaultEffectB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetDefaultEffectB` método recupera o efeito padrão. Esse método é equivalente a [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), mas recebe um **valor BSTR** em vez de um GUID.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Recebe um valor **BSTR** que representa o GUID do efeito padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O método aloca memória para a cadeia de caracteres. O aplicativo deve chamar **SysFreeString** para liberar a memória.

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

 

 




