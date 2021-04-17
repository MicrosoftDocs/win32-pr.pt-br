---
description: 'O método GetDefaultEffectB recupera o efeito padrão. Esse método é equivalente a IAMTimeline:: GetDefaultEffect, mas recebe um valor BSTR em vez de um GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'Método IAMTimeline:: GetDefaultEffectB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752876"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>Método IAMTimeline:: GetDefaultEffectB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetDefaultEffectB` método recupera o efeito padrão. Esse método é equivalente a [**IAMTimeline:: GetDefaultEffect**](iamtimeline-getdefaulteffect.md), mas recebe um valor **BSTR** em vez de um GUID.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Recebe um valor **BSTR** que representa o GUID do efeito padrão.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




