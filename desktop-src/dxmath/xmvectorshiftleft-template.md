---
description: Desloca um vetor à esquerda por um determinado número de elementos de 32 bits, preenchendo os elementos desocupados com elementos de um segundo vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modelo XMVectorShiftLeft (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab92e2fb64a101251a7531ca1d96b8b06f3e9af6e2b7dabe7958673a61bd8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499275"
---
# <a name="xmvectorshiftleft-template"></a>Modelo XMVectorShiftLeft

Desloca um vetor à esquerda por um determinado número de elementos de 32 bits, preenchendo os elementos desocupados com elementos de um segundo vetor.

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

\[em \] Vetor para deslocar para a esquerda.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[em \] Vector usado para preencher os componentes desocupados da V1 depois que ele é deslocado para a esquerda.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o deslocado e preenchido em [**XMVECTOR.**](xmvector-data-type.md)

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo [**de XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) em que o *argumento Elements* é um valor de modelo.

> [!Note]  
> O `XMVectorShiftLeft` modelo é novo para DirectXMath e não está disponível para XNAMath 2.x.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
