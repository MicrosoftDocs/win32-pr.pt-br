---
description: Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a maior das duas instâncias. O tipo de dados dos argumentos e o valor de retorno é o mesmo.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Modelo XMMax (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362f486861400223024da5442c5103722bf35dcf8cba715da1397ad4b54c19b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117966"
---
# <a name="xmmax-template"></a>Modelo XMMax

Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a maior das duas instâncias. O tipo de dados dos argumentos e o valor de retorno é o mesmo.

## <a name="syntax"></a>Sintaxe

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*Um*
</dt> <dd>

\[em \] Especifica o primeiro de dois objetos.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[em \] Especifica os dois de dois objetos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o maior dos dois objetos de entrada.

## <a name="remarks"></a>Comentários

`XMMax` é um modelo e o tipo T é especificado quando o modelo é instautado.

> [!Note]  
> O `XMMax` modelo é novo para DirectXMath e não está disponível para XNAMath 2.x. `XMMax` está disponível como uma macro no XNAMath 2.x.

 

> [!Note]  
> O ideal é usar std::max em vez de `XMMax` . Para evitar conflitos com Windows com std::max, você precisa definir NOMINMAX antes de incluir Windows \# de segurança.

 

**Namespace**: usar o DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. Com suporte para aplicativos da área de trabalho Win32, aplicativos Windows Store e Windows Phone 8 aplicativos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de modelo da biblioteca DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMin**](xmmin-template.md)
</dt> </dl>

 

 




