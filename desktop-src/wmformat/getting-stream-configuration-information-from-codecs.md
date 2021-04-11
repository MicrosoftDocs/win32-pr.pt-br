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
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365735"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Obtendo informações de configuração de fluxo de codecs

Para fluxos de áudio e vídeo que usam os codecs de áudio e vídeo do Windows Media, você deve obter os valores para as estruturas de configuração de fluxo do codec que deseja usar. Embora seja possível definir esses valores por conta própria, usar os codecs garante que os valores sejam precisos. Você não deve alterar os valores nessas estruturas, a menos que a documentação recomende especificamente uma alteração específica.

As informações dos codecs vêm na forma de formatos de codec. Cada formato de codec é um formato de fluxo único com suporte pelo codec. Para obter mais informações sobre formatos de fluxo, consulte [formatos](formats.md).

Você pode solicitar informações dos codecs de mídia do Windows usando as interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) do objeto do Gerenciador de perfis. Para obter a interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de um objeto do Gerenciador de perfis, chame a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Chame **QueryInterface** em **IWMProfileManager** para obter **IWMCodecInfo3**.

As seções a seguir descrevem como obter as informações necessárias.



| Seção                                                                                                | Descrição                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para enumerar todos os codecs de mídia do Windows instalados](to-enumerate-all-installed-windows-media-codecs.md) | Descreve como usar os métodos das interfaces **IWMCodecInfo** e **IWMCodecInfo2** para recuperar o nome e o índice de codec de cada codec de mídia do Windows instalado. |
| [Para enumerar formatos de codec](to-enumerate-codec-formats.md)                                           | Descreve como obter objetos de configuração de fluxo de codecs para uso em seus perfis.                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> </dl>

 

 




