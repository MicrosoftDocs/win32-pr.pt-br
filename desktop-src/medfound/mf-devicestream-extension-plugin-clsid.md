---
description: Especifica o CLSID de um plug-in de pós-processamento para um dispositivo de captura de vídeo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Atributo MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781635"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>\_ \_ \_ Atributo CLSID de plugin de extensão MF DEVICESTREAM \_

Especifica o CLSID de um plug-in de pós-processamento para um dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Um plug-in de pós-processamento é um MFT que processa a imagem de vídeo depois que ela é capturada. O fornecedor de hardware pode incluir um plug-in de pós-processamento como parte do pacote de instalação. Nesse caso, a fonte de captura de vídeo define \_ o \_ \_ atributo CLSID do plug-in de extensão MF DEVICESTREAM \_ para o CLSID do plug-in.

Para obter esse atributo, faça o seguinte:

1.  Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.
3.  Chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) para obter o atributo.

Para criar o plug-in, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
