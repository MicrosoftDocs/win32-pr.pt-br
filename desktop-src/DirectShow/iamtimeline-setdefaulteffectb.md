---
description: 'O método SetDefaultEffectB define o efeito padrão. Esse método é equivalente a IAMTimeline:: SetDefaultEffect, mas usa um valor BSTR, em vez de um ponteiro para um GUID.'
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'Método IAMTimeline:: SetDefaultEffectB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a8722a195078cb032285e4ea2ac449ad045d54f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747565"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a>Método IAMTimeline:: SetDefaultEffectB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetDefaultEffectB` método define o efeito padrão. Esse método é equivalente a [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md), mas usa um valor BSTR, em vez de um ponteiro para um GUID.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Valor BSTR que representa o GUID do efeito padrão.

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

 

 




