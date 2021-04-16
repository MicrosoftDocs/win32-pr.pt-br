---
description: O método SetDefaultTransition define a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'Método IAMTimeline:: SetDefaultTransition (QEdit. h)'
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
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757888"
---
# <a name="iamtimelinesetdefaulttransition-method"></a>Método IAMTimeline:: SetDefaultTransition

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

*pGuid* 
</dt> <dd>

Ponteiro para uma variável que contém o GUID da transição padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se você não definir uma transição padrão ou se a transição que você especificar como padrão causar um erro, o DES usará sua própria transição padrão.

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

 

 




