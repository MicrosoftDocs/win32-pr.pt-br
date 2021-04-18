---
description: O \_ método Get matiz recupera o valor de matiz para o qual fazer a chave. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ matiz.
ms.assetid: d37fedd6-f29f-4f16-821b-c5f8520c4e12
title: 'Método IDxtKey:: get_Hue (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72058076e87f1a8738f3153ee8095eefb4ebce8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758513"
---
# <a name="idxtkeyget_hue-method"></a>Método IDxtKey:: get \_ matiz

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Hue` método recupera o valor de matiz para o qual fazer a chave. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ matiz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Hue(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o valor de matiz para o qual fazer a chave.

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

[**IDxtKey:: obter \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




