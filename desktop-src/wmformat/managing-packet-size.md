---
title: Gerenciamento do tamanho do pacote
description: Gerenciamento do tamanho do pacote
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows SDK de Formato de Mídia, gerenciando tamanhos de pacotes
- Windows SDK de Formato de Mídia, tamanhos de pacotes
- perfis, tamanhos de pacotes
- perfis, gerenciando tamanhos de pacotes
- pacotes, tamanhos
- packets,interface IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b8755eccdcc0042532be4359cd51fce2ef379b51882e6cc4585c48c8769a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846708"
---
# <a name="managing-packet-size"></a>Gerenciamento do tamanho do pacote

O autor foi projetado para gerenciar o tamanho dos pacotes internamente. No entanto, você pode ter requisitos específicos para seu aplicativo que chamam algum controle manual sobre o tamanho dos pacotes nos arquivos ASF que você escreve. O SDK Windows Formato de Mídia do Windows fornece duas interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) que permitem controlar o tamanho máximo e mínimo dos pacotes.

Ambas as interfaces de tamanho de pacote são expostas no objeto de perfil. Eles também estão disponíveis para o objeto de leitor. Assim como com outras interfaces relacionadas ao perfil, o leitor pode acessar apenas os métodos de leitura.

O tamanho dos pacotes tem algum efeito no desempenho. Em geral, quanto menor o tamanho do pacote, mais fragmentados os dados estão dentro de um arquivo. Quanto mais fragmentado for um arquivo, menos eficiente será reconstruí-lo. Em um cenário de streaming, isso pode não ser uma consideração importante, pois o processo de leitura de um arquivo de uma fonte de Internet geralmente é ineficiente. No entanto, ao lidar com um arquivo localmente, isso pode ser uma consideração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPacketSize Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**IWMPacketSize2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




