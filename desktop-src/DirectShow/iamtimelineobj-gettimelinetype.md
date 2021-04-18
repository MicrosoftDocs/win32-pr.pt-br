---
description: O método gettimelinetype recupera o tipo do objeto.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'Método IAMTimelineObj:: gettimelinetype (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785493"
---
# <a name="iamtimelineobjgettimelinetype-method"></a>Método IAMTimelineObj:: gettimelinetype

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetTimelineType` método recupera o tipo do objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe um membro do tipo enumerado de [**\_ \_ tipo principal da linha do tempo**](timeline-major-type.md) , indicando o tipo de objeto.

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
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




