---
description: O método remove remove esse objeto da linha do tempo (incluindo subobjetos, mas não filhos), para reinserção em outro lugar.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Método IAMTimelineObj:: Remove (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761762"
---
# <a name="iamtimelineobjremove-method"></a>Método IAMTimelineObj:: Remove

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `Remove` método remove esse objeto da linha do tempo (incluindo subobjetos, mas não filhos), para reinserção em outro lugar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Chame esse método somente se o aplicativo inserir imediatamente o objeto de volta na linha do tempo. É uma operação inválida para chamar esse método sem, em seguida, reinserir o objeto. Para remover um objeto permanentemente, chame [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md).

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

 

 




