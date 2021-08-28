---
description: Gira o vetor para a direita em um determinado número de elementos de 32 bits.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Modelo XMVectorRotateRight (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47017982af6bb61212129665010d403bd9db898c65056110c4d2f40a5f8a9362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984486"
---
# <a name="xmvectorrotateright-template"></a>Modelo XMVectorRotateRight

Gira o vetor para a direita em um determinado número de elementos de 32 bits.

## <a name="syntax"></a>Sintaxe

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[em \] Vector para girar para a direita.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o [**XMVECTOR girado.**](xmvector-data-type.md)

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo [**de XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) em que o *argumento Elements* é um valor de modelo.

> [!Note]  
> O `XMVectorRotateRight` modelo é novo para DirectXMath e não está disponível para XNAMath 2.x.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
