---
description: O método addprop adiciona uma propriedade ao setter da propriedade, com uma matriz de pares time-Value que definem o valor da propriedade em um intervalo de tempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Método IPropertySetter:: addprop (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759535"
---
# <a name="ipropertysetteraddprop-method"></a>Método IPropertySetter:: addprop

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `AddProp` método adiciona uma propriedade ao setter da propriedade, com uma matriz de pares time-Value que definem o valor da propriedade em um intervalo de tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Parâmetro* \[ no\]
</dt> <dd>

[**Dexter \_**](dexter-param.md) A estrutura do parâmetro que especifica a propriedade. O membro **nValores** da estrutura deve ser igual ao tamanho da matriz fornecida no parâmetro *paValue* .

</dd> <dt>

*paValue* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) que contêm pares de tempo-valor. A matriz deve estar em ordem de tempo crescente. Os tempos são relativos à hora de início do efeito ou da transição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A primeira estrutura de [**\_ valor de Dexter**](dexter-value.md) deve especificar um tempo de referência de zero e um sinalizador de interpolação (**DwInterp**) do **\_ salto DEXTERF** ou o método retorna um erro.

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




