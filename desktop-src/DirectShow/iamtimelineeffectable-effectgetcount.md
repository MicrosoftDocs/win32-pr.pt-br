---
description: O método EffectGetCount recupera o número de efeitos neste objeto.
ms.assetid: 6cf3b5b1-f38f-4ee1-8567-3c55f4f89cbb
title: 'Método IAMTimelineEffectable:: EffectGetCount (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b55ada9acf0db76a1e8017185bb74851356add3aa3b3b06e92980b2d6beafea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400983"
---
# <a name="iamtimelineeffectableeffectgetcount-method"></a>Método IAMTimelineEffectable:: EffectGetCount

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EffectGetCount` método recupera o número de efeitos neste objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EffectGetCount(
   long *pCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCount* 
</dt> <dd>

Recebe o número de efeitos.

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

[**Interface IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




