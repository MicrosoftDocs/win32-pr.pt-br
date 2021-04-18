---
description: O método SetSubObjectGUID especifica o GUID do subobjeto associado a esse objeto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'Método IAMTimelineObj:: SetSubObjectGUID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758060"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a>Método IAMTimelineObj:: SetSubObjectGUID

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetSubObjectGUID` método especifica o GUID do subobjeto associado a esse objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* 
</dt> <dd>

GUID do subobjeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O mecanismo de processamento cria uma instância do subobjeto conforme necessário.

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

 

 




