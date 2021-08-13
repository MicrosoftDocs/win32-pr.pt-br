---
description: Gira o vetor à esquerda por um determinado número de elementos de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modelo XMVectorRotateLeft (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3d2a06f775e99b275d7333816307f494c5b2a4a7cc0183eaddc4ee4cd8950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499399"
---
# <a name="xmvectorrotateleft-template"></a>Modelo XMVectorRotateLeft

Gira o vetor à esquerda por um determinado número de elementos de 32 bits.

## <a name="syntax"></a>Sintaxe

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[em \] Vetor para girar para a esquerda.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o [**XMVECTOR girado.**](xmvector-data-type.md)

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo [**de XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) em que o *argumento Elements* é um valor de modelo.

> [!Note]  
> O `XMVectorRotateLeft` modelo é novo para DirectXMath e não está disponível para XNAMath 2.x.

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
