---
description: Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a maior das duas instâncias. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Modelo XMMax (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760588"
---
# <a name="xmmax-template"></a>Modelo XMMax

Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a maior das duas instâncias. O tipo de dados dos argumentos e o valor de retorno são os mesmos.

## <a name="syntax"></a>Sintaxe

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*um*
</dt> <dd>

\[em \] especifica o primeiro de dois objetos.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[em \] especifica os dois de dois objetos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o maior dos dois objetos de entrada.

## <a name="remarks"></a>Comentários

`XMMax` é um modelo e o tipo T é especificado quando o modelo é instanciado.

> [!Note]  
> O `XMMax` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x. `XMMax` está disponível como uma macro no XNAMath 2. x.

 

> [!Note]  
> Idealmente, use std:: Max em vez de `XMMax` . Para evitar conflitos com cabeçalhos do Windows com std:: Max, você precisa \# definir NOMINMAX antes de incluir cabeçalhos do Windows.

 

**Namespace**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de modelo de biblioteca DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMin**](xmmin-template.md)
</dt> </dl>

 

 




