---
description: Swizzles um vetor.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modelo XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810911"
---
# <a name="xmvectorswizzle-template"></a>Modelo XMVectorSwizzle

Swizzles um vetor.

## <a name="syntax"></a>Sintaxe

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*L*
</dt> <dd>

\[em \] vetor para swizzle.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o swizzled [**XMVECTOR**](xmvector-data-type.md).

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo do [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , em que os argumentos *swizzle \** são valores de modelo.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` e `XM_SWIZZLE_W` são constantes que são avaliadas como 0, 1, 2 e 3, respectivamente, para uso com `XMVectorSwizzle` . Isso é idêntico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` e `XM_PERMUTE_0W` .

> [!Note]  
> O `XMVectorSwizzle` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.

 

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
</dt> </dl>

 

 
