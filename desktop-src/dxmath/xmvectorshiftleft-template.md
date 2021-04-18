---
description: Desloca um vetor à esquerda por um determinado número de elementos de 32 bits, preenchendo os elementos vagados com elementos de um segundo vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modelo XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752734"
---
# <a name="xmvectorshiftleft-template"></a>Modelo XMVectorShiftLeft

Desloca um vetor à esquerda por um determinado número de elementos de 32 bits, preenchendo os elementos vagados com elementos de um segundo vetor.

## <a name="syntax"></a>Sintaxe

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[em \] vetor para deslocar para a esquerda.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[em \] vetor usado para preencher os componentes vagados do v1 depois que ele é deslocado para a esquerda.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna a mudança e a preenchida em [**XMVECTOR**](xmvector-data-type.md).

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo do [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , em que o argumento *Elements* é um valor de modelo.

> [!Note]  
> O `XMVectorShiftLeft` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
