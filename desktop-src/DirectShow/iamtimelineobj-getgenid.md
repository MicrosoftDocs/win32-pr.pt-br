---
description: O método GetGenID recupera o identificador gerado do objeto. O identificador é um número reservado; os aplicativos não devem usá-lo.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Método IAMTimelineObj:: GetGenID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c48e13167e947404d0975d9f2b3695faef2e284625a287360996b4d07226bb84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400734"
---
# <a name="iamtimelineobjgetgenid-method"></a>Método IAMTimelineObj:: GetGenID

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetGenID` método recupera o identificador gerado do objeto. O identificador é um número reservado; os aplicativos não devem usá-lo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe o identificador gerado.

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
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




