---
description: 'Método IAMTimelineObj:: SetDirtyRange-não implementado.'
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: 'Método IAMTimelineObj:: SetDirtyRange (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1cd03802aa019e6da81f2667dddd3a5bede67ad70c98a82e843ee0f05c36e956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086816"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a>Método IAMTimelineObj:: SetDirtyRange

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Não implementado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Reservado.

</dd> <dt>

*Parar* 
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

 

 




