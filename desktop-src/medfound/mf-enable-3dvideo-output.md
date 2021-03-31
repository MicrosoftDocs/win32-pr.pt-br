---
description: Especifica como uma Media Foundation transformação (MFT) deve gerar um fluxo de vídeo 3D estereoscópico.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Atributo MF_ENABLE_3DVIDEO_OUTPUT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827625"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>\_Atributo de saída MF Enable \_ 3DVIDEO \_

Especifica como uma Media Foundation transformação (MFT) deve gerar um fluxo de vídeo 3D estereoscópico.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor do atributo é um membro da enumeração [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .

Esse atributo se aplica somente se o MFT retornar **true** para o atributo [ \_ \_ 3DVIDEO de suporte do MFT](mft-support-3dvideo.md) .

Para obter ou definir este atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global do MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




