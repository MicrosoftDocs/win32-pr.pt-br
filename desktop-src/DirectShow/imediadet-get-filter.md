---
description: O método \_ get Filter recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: Método IMediaDet::get_Filter (Qedit.h)
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
ms.openlocfilehash: c3d4622438dbb8c8dfc54183550c274fcd4555de8b75435b85bbbebfae9c2c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083756"
---
# <a name="imediadetget_filter-method"></a>Método filter IMediaDet::get \_

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

Recebe um ponteiro para a interface **IUnknown do** filtro. Se nenhum filtro de origem estiver em uso, o valor será definido como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Quando o método retorna, se *\* ppVal* não for **NULL,** a interface **IUnknown** terá uma contagem de referência pendente. Libere a interface quando terminar de usá-la.

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

[**IMediaDet Interface**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




