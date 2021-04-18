---
description: Os Estados de amostra definem operações de amostragem de textura, como endereçamento de textura e filtragem de textura.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumeração D3DSAMPLERSTATETYPE (D3D9Types. h)
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
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802091"
---
# <a name="d3dsamplerstatetype-enumeration"></a>Enumeração D3DSAMPLERSTATETYPE

Os Estados de amostra definem operações de amostragem de textura, como endereçamento de textura e filtragem de textura. Alguns Estados de amostra configuram o processamento de vértice e algum processamento de pixel de configuração. Os Estados de amostra podem ser salvos e restaurados usando stateblocks (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintaxe


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

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**Endereço de D3DSAMP \_**
</dt> <dd>

Textura – modo de endereço para a coordenada u. O padrão é D3DTADDRESS \_ Wrap. Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**
</dt> <dd>

Textura – modo de endereço para a coordenada v. O padrão é D3DTADDRESS \_ Wrap. Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**
</dt> <dd>

Textura – modo de endereço para a coordenada w. O padrão é D3DTADDRESS \_ Wrap. Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**\_BORDERCOLOR D3DSAMP**
</dt> <dd>

Cor da borda ou tipo [**D3DCOLOR**](d3dcolor.md). A cor padrão é 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**
</dt> <dd>

Filtro de ampliação do tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). O valor padrão é D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**
</dt> <dd>

Filtro minificação do tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). O valor padrão é D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**
</dt> <dd>

Filtro de mipmap a ser usado durante o minificação. Consulte [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). O valor padrão é D3DTEXF \_ None.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**
</dt> <dd>

Mipmap de diferença de nível de detalhes. O valor padrão é zero.

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**
</dt> <dd>

índice de nível de detalhe do maior mapa a ser usado. Os valores variam de 0 a (n-1), em que 0 é o maior. O valor padrão é zero.

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**
</dt> <dd>

Anisotropy de máximo DWORD. Os valores variam de 1 até o valor especificado no membro **MaxAnisotropy** da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . O valor padrão é 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**
</dt> <dd>

Valor de correção gama. O valor padrão é 0, o que significa que o gama é 1,0 e nenhuma correção é necessária. Caso contrário, esse valor significa que a amostra deve assumir o gama de 2,2 no conteúdo e convertê-lo em linear (gama 1,0) antes de apresentá-lo ao sombreador de pixel.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**
</dt> <dd>

Quando uma textura Multielemento é atribuída à amostra, isso indica qual índice de elemento usar. O valor padrão é 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**
</dt> <dd>

Deslocamento de vértice no mapa de substituição de amostra. Essa é uma constante usada pelo Tessellator, seu valor padrão é 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
