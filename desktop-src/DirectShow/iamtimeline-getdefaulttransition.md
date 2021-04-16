---
description: O método GetDefaultTransition recupera a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Método IAMTimeline:: GetDefaultTransition (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750272"
---
# <a name="iamtimelinegetdefaulttransition-method"></a>Método IAMTimeline:: GetDefaultTransition

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetDefaultTransition` método recupera a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Recebe o GUID da transição padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




