---
description: O método getgroupname recupera o nome definido pelo aplicativo do grupo.
ms.assetid: 402e97d9-abb5-4d8e-8735-1b06d60ab225
title: 'Método IAMTimelineGroup:: getgroupname (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 78e3fc736ece3f4a8ebea1c688ce2bc5099f497c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775612"
---
# <a name="iamtimelinegroupgetgroupname-method"></a>Método IAMTimelineGroup:: getgroupname

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetGroupName` método recupera o nome definido pelo aplicativo do grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGroupName(
  [out, retval] BSTR *pGroupName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGroupName* \[ out, retval\]
</dt> <dd>

Recebe o nome do grupo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O método aloca memória para a cadeia de caracteres. O aplicativo deve chamar **SysFreeString** para liberar a memória.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




