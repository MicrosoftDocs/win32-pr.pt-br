---
description: Sinalizadores de perfil que definem as configurações de fluxo para a topologia de transcodificação. Os sinalizadores são definidos na enumeração MF \_ transcodificar \_ \_ sinalizadores de perfil \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Atributo MF_TRANSCODE_ADJUST_PROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761427"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>\_Atributo de \_ perfil de ajuste de TRANScodificação MF \_

Sinalizadores de perfil que definem as configurações de fluxo para a topologia de transcodificação. Os sinalizadores são definidos na enumeração [**MF \_ transcodificar \_ \_ \_ sinalizadores de perfil**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Um aplicativo pode definir esse atributo no nível de contêiner no perfil transcodificar. Se esse atributo for definido, a função [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) alterará os atributos de fluxo durante a compilação da topologia, dependendo do sinalizador especificado. Por exemplo, se o aplicativo especificar o **sinalizador \_ \_ padrão do \_ perfil \_ de ajuste de transcodificação MF** , as configurações de fluxo especificadas pelo aplicativo serão usadas para criar o perfil.

Para o fluxo de vídeo, a taxa de quadros é atualizada com base na origem da mídia. Se o aplicativo não especificar o modo entrelaçado, o perfil será atualizado para usar quadros progressivos por padrão.

Se o aplicativo especificar o sinalizador de **\_ uso de \_ \_ \_ \_ \_ atributos de origem MF transcodificar** , os atributos de fluxo ausentes serão copiados da origem de mídia de entrada para as configurações de fluxo no perfil transcodificar.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificação](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile:: setcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




