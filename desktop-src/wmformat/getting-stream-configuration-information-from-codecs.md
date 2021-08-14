---
title: Obtendo informações de configuração de fluxo de codecs
description: Obtendo informações de configuração de fluxo de codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- fluxos, configurações de codecs
- codecs, obtendo configurações de fluxo de
- fluxos, formatos de codec
- codecs, formatos
- fluxos, interface IWMCodecInfo
- IWMCodecInfo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10cd131bfd263e0e9a0616b6fa9b59b3f3b03ace30a199b8b79f8b3c3f3f09f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433862"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Obtendo informações de configuração de fluxo de codecs

para fluxos de áudio e vídeo que usam os codecs de áudio e vídeo de mídia Windows, você deve obter os valores para as estruturas de configuração de fluxo do codec que deseja usar. Embora seja possível definir esses valores por conta própria, usar os codecs garante que os valores sejam precisos. Você não deve alterar os valores nessas estruturas, a menos que a documentação recomende especificamente uma alteração específica.

As informações dos codecs vêm na forma de formatos de codec. Cada formato de codec é um formato de fluxo único com suporte pelo codec. Para obter mais informações sobre formatos de fluxo, consulte [formatos](formats.md).

você pode solicitar informações dos codecs de mídia Windows usando as interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) do objeto do gerenciador de perfis. Para obter a interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de um objeto do Gerenciador de perfis, chame a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Chame **QueryInterface** em **IWMProfileManager** para obter **IWMCodecInfo3**.

As seções a seguir descrevem como obter as informações necessárias.



| Seção                                                                                                | Descrição                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [para enumerar todos os codecs de mídia do Windows instalados](to-enumerate-all-installed-windows-media-codecs.md) | descreve como usar os métodos das interfaces **IWMCodecInfo** e **IWMCodecInfo2** para recuperar o nome e o índice de codec de cada Windows codec de mídia instalado. |
| [Para enumerar formatos de codec](to-enumerate-codec-formats.md)                                           | Descreve como obter objetos de configuração de fluxo de codecs para uso em seus perfis.                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configurando Fluxos**](configuring-streams.md)
</dt> </dl>

 

 




