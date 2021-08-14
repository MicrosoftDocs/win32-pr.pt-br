---
description: Especifica como o sink de mídia ASF deve ser aplicado Windows DRM de Mídia.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed62f62a5d03d7fe938101d9837bd8ed9bccefe69b2bf30e0566ea0b471e37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874340"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>Propriedade \_ DRMACTION MFPKEY ASFMEDIASINK \_

Especifica como o sink de mídia ASF deve ser aplicado Windows DRM de Mídia.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da enumeração [**\_ MFSINK WMDRIACTION.**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction)

Você pode usar esse atributo para configurar o sink de mídia do ASF. O uso depende de qual função você chama para criar o sink de mídia do ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)consulte o ponteiro [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para a interface **IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)chame [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) no ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado no parâmetro *pContentInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
