---
description: O método GetSubObject recupera o subobjeto associado a esse objeto.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'Método IAMTimelineObj:: GetSubObject (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754248"
---
# <a name="iamtimelineobjgetsubobject-method"></a>Método IAMTimelineObj:: GetSubObject

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSubObject` método recupera o subobjeto associado a esse objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe um ponteiro para a interface **IUnknown** do subobjeto. Se o objeto não tiver um subobjeto, o valor será definido como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Cada objeto Timeline pode conter um ponteiro para um subobjeto associado.

Se o valor retornado em *PVal* não for **NULL**, a interface **IUnknown** terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

 

 




