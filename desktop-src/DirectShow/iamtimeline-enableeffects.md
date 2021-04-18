---
description: O método EnableEffects habilita ou desabilita todos os efeitos na linha do tempo. Se os efeitos estiverem desabilitados, eles permanecerão na linha do tempo, mas não serão renderizados.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Método IAMTimeline:: EnableEffects (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766308"
---
# <a name="iamtimelineenableeffects-method"></a>Método IAMTimeline:: EnableEffects

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EnableEffects` método habilita ou desabilita todos os efeitos na linha do tempo. Se os efeitos estiverem desabilitados, eles permanecerão na linha do tempo, mas não serão renderizados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valor booliano que especifica se os efeitos devem ser habilitados ou desabilitados. Se **for true**, os efeitos serão habilitados. Se **for false**, os efeitos serão desabilitados.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




