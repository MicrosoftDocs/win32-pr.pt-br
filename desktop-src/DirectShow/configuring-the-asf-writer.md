---
description: Configurando o gravador ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configurando o gravador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3d28b3b6178a383909f53a98fef98a5c3e69297f71615010f505d28b77375a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871696"
---
# <a name="configuring-the-asf-writer"></a>Configurando o gravador ASF

Quando o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) é criado, ele é configurado automaticamente com o \_ perfil WMProfile V80 \_ 256Video. esse perfil usa os codecs Windows mídia de áudio e Windows vídeo da mídia 8, que não são tão recentes quanto os codecs da série Windows Media 9. é recomendável criar um perfil personalizado que usa os codecs da série Windows Media 9 e configurar o gravador ASF do WM com o perfil personalizado, conforme descrito em [configurando perfis e outras propriedades de arquivo asf](configuring-profiles-and-other-asf-file-properties.md). Você deve adicionar o filtro do gravador ASF do WM ao grafo de filtro antes de configurar o filtro e configurar o filtro antes de conectá-lo a qualquer outro filtro.

Todos os dados de entrada devem ter carimbo de data/hora e todos os Pins de entrada devem ser conectados antes que o filtro possa ser executado ou pausado. Portanto, se você configurar o filtro com um perfil que tenha um fluxo de áudio e um fluxo de vídeo, o filtro criará um áudio e um pino de entrada de vídeo, e ambos os Pins deverão ser conectados antes que o filtro possa ser executado. como o SDK do formato de mídia Windows requer um fluxo de áudio para funcionar, o gravador ASF do WM sempre deve ter um pin de áudio de entrada, mesmo se for para um fluxo fictício, ou seja, um fluxo de áudio sem taxa de baixa de bits, com áudio.

Adicionando extensões de unidade de dados

Você pode configurar um fluxo de perfil para extensões de unidade de dados, como códigos de tempo SMPTE, antes ou depois que o filtro está conectado, desde que você siga esta ordem de operações:

1.  Adicione uma ou mais extensões de unidade de dados ao fluxo usando **IWMStreamConfig2:: AddDataUnitExtension**.
2.  Chame **IWMProfile:: ReconfigStream** para atualizar o perfil.
3.  Chame [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) com o objeto de perfil atualizado.
4.  Localize o PIN de entrada de vídeo e chame o método [**IAMWMBufferPass:: setnotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) para registrar sua interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida pelo aplicativo.

Quando o grafo for executado, o método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) será chamado para cada quadro e você poderá obter e definir propriedades no exemplo usando seus métodos de interface **INSSBuffer3** .

> [!Note]  
> Em alguns cenários com uso intensivo de processador, como o telecineon inverso, o gravador ASF do WM pode exigir mais buffers de saída do que alguns filtros downstream podem dar suporte. O codificador DV, por exemplo, não aceitará mais de um buffer para seu pino de saída e o mesmo será verdadeiro para o descompactador AVI em determinadas condições. Se você encontrar problemas ao tentar se conectar a esses filtros, ou possivelmente ao executar o grafo, pode ser necessário gravar um filtro intermediário que aceite qualquer número de buffers em seu pino de saída.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



