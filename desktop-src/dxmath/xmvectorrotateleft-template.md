---
description: Gira o vetor à esquerda por um determinado número de elementos de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modelo XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750084"
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

<span id="V"></span><span id="v"></span>*L*
</dt> <dd>

\[em \] vetor para girar para a esquerda.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o [**XMVECTOR**](xmvector-data-type.md)girado.

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo do [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , em que o argumento *Elements* é um valor de modelo.

> [!Note]  
> O `XMVectorRotateLeft` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
