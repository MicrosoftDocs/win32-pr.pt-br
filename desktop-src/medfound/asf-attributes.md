---
description: Atributos ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Atributos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbb8697126ae6882c11526ed9e6cb31e2233b81685c820d200fbd21bab08c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975025"
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
| [**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | define os parâmetros médios de "bucket de vazamentos" para codificar um arquivo de mídia Windows. |
| [**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | define os parâmetros de "bucket de vazamento" de pico para codificar um arquivo de mídia Windows.    |



 

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

 

 



