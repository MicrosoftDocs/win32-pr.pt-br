---
title: Estrutura de D3DX11_PASS_DESC (D3dx11effect. h)
description: Descreve um efeito aprovado, que contém o estado do pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- Estrutura D3DX11_PASS_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968691"
---
# <a name="d3dx11_pass_desc-structure"></a>\_Estrutura desc de Pass D3DX11 \_

Descreve um efeito aprovado, que contém o estado do pipeline.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome dessa passagem (**NULL** se não anônimo).

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotações nesta passagem.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Assinatura do sombreador de vértice ou do sombreador de geometria (se não houver nenhum sombreador de vértice) ou **NULL** se não houver nenhum.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamanho de Singature em bytes.

</dd> <dt>

**StencilRef**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O valor de referência de estêncil usado no estado de estêncil de profundidade.

</dd> <dt>

**SampleMask**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A máscara de exemplo para o estado de mesclagem.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Os fatores de combinação por componente (RGBA) para o estado de mesclagem.

</dd> </dl>

## <a name="remarks"></a>Comentários

D3DX11 \_ Pass \_ DESC é usado com [**ID3DX11EffectPass:: GetDesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

