---
description: Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a menor das duas instâncias. O tipo de dados dos argumentos e o valor de retorno é o mesmo.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modelo XMMin (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2d78b64a66411c31570267c66a7e75171dcf9da039871c07c8bfc31df49149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499851"
---
# <a name="xmmin-template"></a>Modelo XMMin

Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a menor das duas instâncias. O tipo de dados dos argumentos e o valor de retorno é o mesmo.

## <a name="syntax"></a>Sintaxe

``` syntax
template<class T> T XMMin(
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

Retorna o menor dos dois objetos de entrada.

## <a name="remarks"></a>Comentários

`XMMin` é um modelo e o tipo T é especificado quando o modelo é instautado.

> [!Note]  
> O `XMMin` modelo é novo para DirectXMath e não está disponível para XNAMath 2.x. `XMMin` está disponível como uma macro no XNAMath 2.x.

 

> [!Note]  
> O ideal é usar std::min em vez de `XMMin` . Para evitar conflitos com Windows com std::min, você precisa definir NOMINMAX antes de incluir \# Windows de segurança.

 

**Namespace**: usar o DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. Com suporte para aplicativos da área de trabalho win32, aplicativos Windows Store e Windows Phone 8 aplicativos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de modelo da biblioteca DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




