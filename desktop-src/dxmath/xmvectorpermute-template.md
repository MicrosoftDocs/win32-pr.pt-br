---
description: Permuta mudo dos componentes de dois vetores para criar um novo vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modelo XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd3f7071edaf659991c1294d29a154d3a319d5faee982537025e107cf9621f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978666"
---
# <a name="xmvectorpermute-template"></a>Modelo XMVectorPermute

Permuta mudo dos componentes de dois vetores para criar um novo vetor.

## <a name="syntax"></a>Sintaxe

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[no \] primeiro vetor.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[no \] segundo vetor.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o vetor mudo que resultou da combinação dos vetores de origem.

## <a name="remarks"></a>Comentários

Se todos os quatro índices fizerem referência apenas a um único vetor (ou seja, eles estão todos no intervalo de 0-3 ou todos no intervalo de 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) em vez disso para melhorar o desempenho.

Observe que a biblioteca faz uso de especializações de modelo em algumas plataformas para melhorar o desempenho. Nem todo caso de espelho possível é implementado para esses casos especiais, portanto, prefira permudos onde o elemento X do vetor resultante vem do parâmetro v1 em vez do parâmetro v2. Por exemplo, prefira usar `XMVectorPermute<0,1,4,5>(A,B);` para `XMVectorPermute(4,5,0,1)(B,A);` .

Essa função é uma versão de modelo do [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) em que os argumentos de *mudo \** são valores de modelo.

As constantes do [XM \_ permudo \_](ovw-xnamath-reference-constants.md) são fornecidas para uso como valores de entrada para *permutex*,*mudo*,*PermuteZ* e *PermuteW*.

> [!Note]  
> O `XMVectorPermute` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.

 

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

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
