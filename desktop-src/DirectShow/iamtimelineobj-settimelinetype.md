---
description: 'Sem suporte. Chame o método IAMTimeline:: CreateEmptyNode para criar um novo objeto de linha do tempo. Depois que um objeto é criado, você não pode alterar seu tipo.'
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
ms.openlocfilehash: 4592c92c4c40f9fff8294ea546601654afd0111e38fd9f64473512c27b6f1a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400847"
---
# <a name="iamtimelineobjsettimelinetype-method"></a>Método IAMTimelineObj:: settimelinetype

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Sem suporte. Chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) para criar um novo objeto de linha do tempo. Depois que um objeto é criado, você não pode alterar seu tipo.

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

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> </dl>

 

 




