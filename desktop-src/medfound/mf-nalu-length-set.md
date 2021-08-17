---
description: Indica que as informações de comprimento NALU serão enviadas como um BLOB com cada amostra H.264 compactada.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f409cb3c1846667ac21e7d46c559eefb0afc4fe4efbce1f454454d286733157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104382"
---
# <a name="mf_nalu_length_set-attribute"></a>Atributo MF \_ NALU \_ LENGTH \_ SET

Indica que as informações de comprimento NALU serão enviadas como **um BLOB** com cada amostra H.264 compactada.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

De definir esse atributo no tipo de mídia de entrada MEDIASUBTYPE \_ H264.

Definir MF NALU LENGTH SET no tipo de mídia de entrada \_ \_ do decodificador H.264, indicando que cada amostra de entrada terá um comprimento NALU disponível e cada amostra de entrada contém uma imagem primária \_ completa.

O **BLOB que** contém as informações de comprimento NALU pode ser recuperado do atributo [MF \_ NALU LENGTH \_ \_ INFORMATION](mf-nalu-length-information.md) no exemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




