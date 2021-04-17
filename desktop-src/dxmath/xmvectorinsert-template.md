---
description: Gira um vetor à esquerda por um determinado número de componentes de 32 bits e insere os elementos selecionados desse resultado em outro vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modelo XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748655"
---
# <a name="xmvectorinsert-template"></a>Modelo XMVectorInsert

Gira um vetor à esquerda por um determinado número de componentes de 32 bits e insere os elementos selecionados desse resultado em outro vetor.

## <a name="syntax"></a>Sintaxe

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*VD*
</dt> <dd>

\[em \] vetor para inserir.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*VS*
</dt> <dd>

\[em \] vetor para girar para a esquerda.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o [**XMVECTOR**](xmvector-data-type.md) que resulta da rotação e da inserção.

## <a name="remarks"></a>Comentários

Essa função é uma versão de modelo do [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) , em que os argumentos *Select \** são valores de modelo.

Para obter o melhor desempenho, o resultado de `XMVectorInsert` deve ser atribuído de volta para o *VD*.

> [!Note]  
> O `XMVectorInsert` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.

 

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
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
