---
description: Indica que as informações de comprimento de NALU serão enviadas como um BLOB com cada amostra de H. 264 compactada.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Atributo MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781617"
---
# <a name="mf_nalu_length_set-attribute"></a>\_Atributo de \_ conjunto de comprimento MF NALU \_

Indica que as informações de comprimento de NALU serão enviadas como um **blob** com cada amostra de H. 264 compactada.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Defina esse atributo no tipo de mídia de entrada de MEDIASUBTYPE \_ H264.

Defina \_ \_ o tamanho do NALU MF \_ definido no tipo de mídia de entrada do decodificador H. 264, indicando que cada amostra de entrada terá um comprimento de NALU disponível e cada amostra de entrada contém uma imagem primária completa.

O **blob** que contém as informações de comprimento de NALU pode ser recuperado do atributo de [ \_ informações de \_ comprimento \_ MF NALU](mf-nalu-length-information.md) no exemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




