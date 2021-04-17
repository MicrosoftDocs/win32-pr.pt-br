---
description: O \_ método Put similaridade especifica o intervalo de dados de cor que se torna transparente. Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey: método de ut_Similarity de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812817"
---
# <a name="idxtkeyput_similarity-method"></a>Método de similaridade IDxtKey::p UT \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Similarity` método especifica o intervalo de dados de cor que se torna transparente. Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

Especifica o valor de similaridade. O intervalo válido é de 0 a 100.

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

 

 




