---
description: Tempo de envio base para o coletor de mídia ASF, em milissegundos.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: Propriedade MFPKEY_ASFMEDIASINK_BASE_SENDTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813561"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a>\_ \_ \_ Propriedade sendtime base MFPKEY ASFMEDIASINK

Tempo de envio base para o coletor de mídia ASF, em milissegundos.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Comentários

A hora de envio é a hora em que um pacote ASF é enviado pela rede. Ele não corresponde diretamente à hora da apresentação dos dados no pacote.

Você pode usar essa propriedade para configurar o coletor de mídia ASF. O uso depende de qual função você chama para criar o coletor de mídia ASF:

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

 

 




