---
description: O método IsSmartRecompressFormatSet determina se um formato de recompactação inteligente foi definido para o grupo.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: Método IAMTimelineGroup::IsSmartRecompressFormatSet (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e37dfd551f92e0be10ae80f123ce0df0011aa09d2b74313c6a72b2706d7f8a16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107826"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a>Método IAMTimelineGroup::IsSmartRecompressFormatSet

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `IsSmartRecompressFormatSet` método determina se um formato de recompactação inteligente foi definido para o grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pval* 
</dt> <dd>

Recebe um valor booliana que indica se um formato de compactação foi definido. Se **TRUE**, um formato de compactação foi definido.

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

[**IAMTimelineGroup Interface**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




