---
description: Os estados de amostra definem operações de amostragem de textura, como endereçamento de textura e filtragem de textura.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumeração D3DSAMPLERSTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55e8efe80390f64f2376fd3995e414fed604ec8cb854c14b94f71922e146a32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988876"
---
# <a name="d3dsamplerstatetype-enumeration"></a>Enumeração D3DSAMPLERSTATETYPE

Os estados de amostra definem operações de amostragem de textura, como endereçamento de textura e filtragem de textura. Alguns estados de exemplo configuram o processamento de vértice e algum processamento de pixel de configuração. Os estados de amostra podem ser salvos e restaurados usando stateblocks (consulte Estado de salvar e restaurar blocos de estado [(Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ ADDRESSU**
</dt> <dd>

Modo de endereço de textura para a coordenada u. O padrão é D3DTADDRESS \_ WRAP. Para obter mais informações, [**consulte D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**
</dt> <dd>

Modo de endereço de textura para a coordenada v. O padrão é D3DTADDRESS \_ WRAP. Para obter mais informações, [**consulte D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**
</dt> <dd>

Modo de endereço de textura para a coordenada w. O padrão é D3DTADDRESS \_ WRAP. Para obter mais informações, [**consulte D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**
</dt> <dd>

Cor da borda ou tipo [**D3DCOLOR.**](d3dcolor.md) A cor padrão é 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**
</dt> <dd>

Filtro de ampliação do tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). O valor padrão é D3DTEXF \_ POINT.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**
</dt> <dd>

Filtro de minificação do tipo [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md) O valor padrão é D3DTEXF \_ POINT.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**
</dt> <dd>

Filtro Mipmap a ser usado durante a minificação. Consulte [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). O valor padrão é D3DTEXF \_ NONE.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**
</dt> <dd>

Desvio de nível de detalhes do Mipmap. O valor padrão é zero.

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**
</dt> <dd>

índice de nível de detalhes do maior mapa a ser usado. Os valores variam de 0 a (n a 1), em que 0 é o maior. O valor padrão é zero.

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAX VIP**
</dt> <dd>

DWORD maximum anisoosey. Os valores variam de 1 até o valor especificado no **membro Max Ltda da** estrutura [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) O valor padrão é 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**
</dt> <dd>

Valor de correção gama. O valor padrão é 0, o que significa que gama é 1,0 e nenhuma correção é necessária. Caso contrário, esse valor significa que o amostrador deve assumir gama de 2,2 no conteúdo e convertê-lo em linear (gama 1,0) antes de apresentá-lo ao sombreador de pixel.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**ELEMENTO D3DSAMPINDEX \_**
</dt> <dd>

Quando uma textura multielemento é atribuída ao sampler, isso indica qual índice de elemento usar. O valor padrão é 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**
</dt> <dd>

Deslocamento de vértice no mapa de deslocamento pré-mpado. Essa é uma constante usada pelo mosaico, seu valor padrão é 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
