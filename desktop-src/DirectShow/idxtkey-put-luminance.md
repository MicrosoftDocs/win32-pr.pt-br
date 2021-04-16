---
description: O \_ método de luminância Put especifica o valor de luminância no qual a chave deve ser inserida. Essa propriedade só se aplica quando o tipo de chave é \_ luminância DXTKEY.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'IDxtKey: método de ut_Luminance de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782233"
---
# <a name="idxtkeyput_luminance-method"></a>Método de luminância IDxtKey::p UT \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Luminance` método especifica o valor de luminância para a chave. Essa propriedade só se aplica quando o tipo de chave é \_ luminância DXTKEY.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

O valor de luminância para a chave. O intervalo válido é de 0 a 100.

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

[**Interface IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey::p UT \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




