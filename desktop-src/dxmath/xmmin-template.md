---
description: Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que oferece suporte a uma sobrecarga de < e retorna a menor das duas instâncias. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modelo XMMin (DirectXMath. h)
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

Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que oferece suporte a uma sobrecarga de < e retorna a menor das duas instâncias. O tipo de dados dos argumentos e o valor de retorno são os mesmos.

## <a name="syntax"></a>Sintaxe

``` syntax
template<class T> T XMMin(
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

Retorna o menor dos dois objetos de entrada.

## <a name="remarks"></a>Comentários

`XMMin` é um modelo e o tipo T é especificado quando o modelo é instanciado.

> [!Note]  
> O `XMMin` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x. `XMMin` está disponível como uma macro no XNAMath 2. x.

 

> [!Note]  
> Idealmente, use std:: min em vez de `XMMin` . para evitar conflitos com cabeçalhos de Windows com std:: min, você precisa \# definir NOMINMAX antes de incluir cabeçalhos de Windows.

 

**Namespace**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. com suporte para aplicativos de área de trabalho do Win32, aplicativos da Windows store e aplicativos Windows Phone 8.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de modelo de biblioteca DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




