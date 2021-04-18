---
description: 'Não há suporte. Chame o método IAMTimeline:: CreateEmptyNode para criar um novo objeto de linha do tempo. Depois que um objeto é criado, você não pode alterar seu tipo.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'Método IAMTimelineObj:: settimelinetype (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812981"
---
# <a name="iamtimelineobjsettimelinetype-method"></a>Método IAMTimelineObj:: settimelinetype

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Não há suporte. Chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) para criar um novo objeto de linha do tempo. Depois que um objeto é criado, você não pode alterar seu tipo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* 
</dt> <dd>

Reservado.

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> </dl>

 

 




