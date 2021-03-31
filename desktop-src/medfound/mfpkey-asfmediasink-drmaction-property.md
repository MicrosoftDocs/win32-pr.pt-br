---
description: Especifica como o coletor de mídia ASF deve aplicar o DRM do Windows Media.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Propriedade MFPKEY_ASFMEDIASINK_DRMACTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663815"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>\_Propriedade MFPKEY ASFMEDIASINK \_ DRMACTION

Especifica como o coletor de mídia ASF deve aplicar o DRM do Windows Media.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da enumeração [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .

Você pode usar esse atributo para configurar o coletor de mídia ASF. O uso depende de qual função você chama para criar o coletor de mídia ASF:

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): consulta o ponteiro [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para a interface **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) no ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado no parâmetro *pContentInfo* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
