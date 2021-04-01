---
description: Define o modo de processamento do MFT Estabilização de Vídeo.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Atributo MF_VIDEODSP_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090860"
---
# <a name="mf_videodsp_mode-attribute"></a>\_Atributo de \_ modo VIDEODSP MF

Define o modo de processamento do [**MFT estabilização de vídeo**](video-stabilization-mft.md).

## <a name="data-type"></a>Tipo de dados

**MFVideoDSPMode** armazenado como **UIINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um valor de enumeração [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Esse atributo pode ser usado para habilitar ou desabilitar a estabilização de imagem e pode ser atualizado para cada exemplo de saída.

Para definir este atributo:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no MFT de estabilização de vídeo para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para definir o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Estabilização de Vídeo MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




