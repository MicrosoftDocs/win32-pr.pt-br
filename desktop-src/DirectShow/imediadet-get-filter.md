---
description: O \_ método obter filtro recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Método IMediaDet:: get_Filter (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782232"
---
# <a name="imediadetget_filter-method"></a>Método de filtro IMediaDet:: get \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Filter` método recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVal* \[ out, retval\]
</dt> <dd>

Recebe um ponteiro para a interface **IUnknown** do filtro. Se nenhum filtro de origem estiver em uso, o valor será definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando o método retornar, se *\* ppVal* não for **NULL**, a interface **IUnknown** terá uma contagem de referência pendente. Libere a interface quando terminar de usá-la.

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

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




