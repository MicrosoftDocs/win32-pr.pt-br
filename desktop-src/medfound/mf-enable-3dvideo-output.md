---
description: Especifica como uma transformação Media Foundation (MFT) deve dar saída a um fluxo de vídeo 3D estereotipado.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed361ef53d628e0970ffa35f9920750c9d3b0f7efbe81a0ef8759e8ba00a45ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013166"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>Atributo MF \_ ENABLE \_ 3DVIDEO \_ OUTPUT

Especifica como uma transformação Media Foundation (MFT) deve dar saída a um fluxo de vídeo 3D estereotipado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor do atributo é um membro da [**enumeração MF3DVideoOutputType.**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype)

Esse atributo se aplica somente se o MFT retornar **TRUE** para o [atributo MFT SUPPORT \_ \_ 3DVIDEO.](mft-support-3dvideo.md)

Para obter ou definir essa chamada de atributo [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o armazenamento de atributo global do MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




