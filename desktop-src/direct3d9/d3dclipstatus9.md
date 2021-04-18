---
description: Descreve o status atual do clipe.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Estrutura D3DCLIPSTATUS9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808325"
---
# <a name="d3dclipstatus9-structure"></a>Estrutura D3DCLIPSTATUS9

Descreve o status atual do clipe.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Membros

<dl> <dt>

**ClipUnion**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Sinalizadores de União de clipe que descrevem o status atual do clipe. Esse membro pode ser um ou mais dos seguintes sinalizadores:



| Valor                                                                                                                                                      | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ tudo**</dt> </dl>          | Combinação de todos os sinalizadores de clipe.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ à esquerda**</dt> </dl>       | Todos os vértices são recortados pelo plano à esquerda do frustum de exibição.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ à direita**</dt> </dl>    | Todos os vértices são recortados pelo plano certo do frustum de exibição.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ superior**</dt> </dl>          | Todos os vértices são recortados pelo plano superior do frustum de exibição.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ inferior**</dt> </dl> | Todos os vértices são recortados pelo plano inferior do frustum de exibição.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ frontal**</dt> </dl>    | Todos os vértices são recortados pelo plano frontal do frustum de exibição.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ voltar**</dt> </dl>       | Todos os vértices são recortados pelo plano de fundo do frustum de exibição.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Planos de recorte definidos pelo aplicativo.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | Planos de recorte definidos pelo aplicativo.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Planos de recorte definidos pelo aplicativo.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Planos de recorte definidos pelo aplicativo.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Planos de recorte definidos pelo aplicativo.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Planos de recorte definidos pelo aplicativo.<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Sinalizadores de interseção de clipe que descrevem o status atual do clipe. Esse membro pode usar os mesmos sinalizadores que ClipUnion.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o recorte é habilitado durante o processamento de vértice (por [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)ou outras funções de desenho), o Direct3D computa um código de clipe para cada vértice. O código do clipe é uma combinação de \_ \* bits D3DCS. Quando um vértice está fora de um plano de recorte específico, o bit correspondente é definido no código de recorte. O Direct3D mantém o status do clipe usando **D3DCLIPSTATUS9**, que tem membros ClipUnion e ClipIntersection. ClipUnion é uma ou bit a bit de todos os códigos de clipe de vértice, e ClipIntersection é um bit e de todos os códigos de clipes de vértice. Os valores iniciais são zero para ClipUnion e 0xFFFFFFFF para ClipIntersection. Quando o \_ recorte de D3DRS é definido como **false**, ClipUnion e ClipIntersection são definidos como zero. O Direct3D atualiza o status do clipe durante chamadas de desenho. Para calcular o status do clipe de um objeto específico, defina ClipUnion e ClipIntersection como seu valor inicial e continue o desenho.

O status do clipe não é atualizado por [**DrawRectPatch**](/windows/desktop/api) e [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) porque não há emulação de software para eles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
