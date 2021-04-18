---
description: Conversor de t/Sink/coletor de Altova
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Conversor de t/Sink/coletor de Altova
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760735"
---
# <a name="teesink-to-sink-converter"></a>Conversor de t/Sink/coletor de Altova

O conversor de Altova/coletor-para-coletor é um filtro baseado em KsProxy, em modo kernel. Ele é usado em gráficos de filtro de televisão de vídeo analógico em que os dados do VBI estão sendo renderizados ou capturados. O filtro é conectado ao upstream para o [filtro de captura de vídeo WDM](wdm-video-capture-filter.md) e fornece um meio eficiente para duplicar fluxos de dados no modo kernel sem as transições caras entre o kernel e o modo de usuário. Ele entrega cada bloco de dados recebidos a todos os Pins de saída, e o codec downstream é responsável por localizar os dados específicos do VBI a serem decodificados.

O conversor de alto/pia/coletor é exibido na categoria de filtro "dispositivos de divisão/divisores de streaming WDM" (AM \_ KSCATEGORY \_ Splitter).

Como esse é um filtro de modo kernel, os aplicativos não podem criá-lo diretamente usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md). Para obter mais informações, consulte [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 
