---
description: O método GetSubObjectGUIDB recupera o GUID do subobjeto associado a esse objeto de linha do tempo. Esse método é equivalente a IAMTimelineObj::GetSubObjectGUID, mas recebe um valor BSTR.
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: Método IAMTimelineObj::GetSubObjectGUIDB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79cf7c6a0b3f162f3f3baee2a46cfc0c2c2b61271b19e57549c73b4faa0594bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155377"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a>Método IAMTimelineObj::GetSubObjectGUIDB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSubObjectGUIDB` método recupera o GUID do subobjeto associado a este objeto de linha do tempo. Esse método é equivalente a [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), mas recebe um **valor BSTR.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recebe uma cadeia de caracteres que representa o GUID do subobjeto.

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

[**IAMTimelineObj Interface**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




