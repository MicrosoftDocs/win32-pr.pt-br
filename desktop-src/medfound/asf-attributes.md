---
description: Atributos ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Atributos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763220"
---
# <a name="asf-attributes"></a>Atributos ASF

### <a name="profile-attributes"></a>Atributos de perfil

Os atributos a seguir se aplicam a perfis ASF.



| Atributo                                                                      | Descrição                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_ASFPROFILE MF \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | Especifica o tamanho máximo do pacote para um arquivo ASF, em bytes. |
| [**\_ASFPROFILE MF \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | Especifica o tamanho mínimo do pacote para um arquivo ASF, em bytes. |



 

### <a name="stream-configuration-attributes"></a>Atributos de configuração de fluxo

Os atributos a seguir se aplicam ao objeto de configuração de fluxo ASF.



| Atributo                                                                              | Descrição                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Define os parâmetros médios de "Bucket de vazamentos" para codificar um arquivo de mídia do Windows. |
| [**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Define o pico dos parâmetros de "Bucket de vazamentos" para codificar um arquivo de mídia do Windows.    |



 

### <a name="media-buffer-attributes"></a>Atributos de buffer de mídia

Os atributos a seguir se aplicam a buffers de mídia para pacotes ASF.



| Atributo                                                                          | Descrição                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_limite de pacotes MFASFSPLITTER \_**](mfasfsplitter-packet-boundary-attribute.md) | Especifica se um buffer contém o início de um pacote ASF (Advanced Systems Format). |



 

### <a name="presentation-descriptor-attributes"></a>Atributos do descritor de apresentação

Para obter uma lista de atributos que se aplicam aos descritores de apresentação do ASF, consulte [atributos de descrição de apresentação](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



