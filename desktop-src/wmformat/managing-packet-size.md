---
title: Gerenciamento do tamanho do pacote
description: Gerenciamento do tamanho do pacote
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- SDK do Windows Media Format, gerenciando tamanhos de pacotes
- SDK do Windows Media Format, tamanhos de pacotes
- perfis, tamanhos de pacotes
- perfis, gerenciando tamanhos de pacotes
- pacotes, tamanhos
- pacotes, interface IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365750"
---
# <a name="managing-packet-size"></a>Gerenciamento do tamanho do pacote

O gravador foi projetado para gerenciar o tamanho dos pacotes internamente. No entanto, você pode ter requisitos específicos para seu aplicativo que chamam algum controle manual sobre o tamanho dos pacotes nos arquivos ASF que você escreve. O Windows Media Format SDK fornece duas interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , que permitem controlar o tamanho máximo e mínimo dos pacotes.

Ambas as interfaces de tamanho de pacote são expostas no objeto de perfil. Eles também estão disponíveis para o objeto leitor. Assim como acontece com outras interfaces relacionadas a perfil, o leitor pode acessar apenas os métodos de leitura.

O tamanho dos pacotes tem algum efeito sobre o desempenho. Em geral, quanto menor o tamanho do pacote, mais fragmentados os dados estão dentro de um arquivo. Quanto mais fragmentado um arquivo for, menos eficiente será reconstruí-lo. Em um cenário de streaming, isso pode não ser uma consideração importante, pois o processo de leitura de um arquivo de uma fonte da Internet geralmente é ineficiente. Ao lidar com um arquivo localmente no entanto, isso pode ser uma consideração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**Interface IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




