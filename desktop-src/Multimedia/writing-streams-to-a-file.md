---
title: Gravando fluxos em um arquivo
description: Gravando fluxos em um arquivo
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- Função AVIFileCreateStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640660"
---
# <a name="writing-streams-to-a-file"></a>Gravando fluxos em um arquivo

Você também pode criar um arquivo que contém fluxos de dados gravando um novo fluxo de dados em um arquivo.

Você pode criar um novo fluxo em um arquivo novo ou existente usando a função [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) . Essa função define um novo fluxo de acordo com as características descritas em uma estrutura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) , cria uma interface de fluxo para o novo fluxo, incrementa a contagem de referência do fluxo e retorna o endereço do ponteiro de interface de fluxo.

Antes de gravar o conteúdo do fluxo, você deve especificar o formato do fluxo. Você pode definir o formato de fluxo usando a função [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) . Ao definir o formato de um fluxo de vídeo, você deve fornecer essa função com uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém as informações apropriadas. Ao definir o formato de um fluxo de áudio, você deve fornecer uma estrutura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contém as informações apropriadas. As informações que você precisa fornecer à função para outros tipos de fluxo dependem do tipo de fluxo e do manipulador de fluxo.

Você pode gravar o conteúdo multimídia em um fluxo usando a função [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) . Essa função copia dados brutos de um buffer fornecido pelo aplicativo para o fluxo especificado. O manipulador de arquivo AVI padrão acrescenta informações ao final de um fluxo. O manipulador WAVE padrão pode gravar dados de wave-áudio em um fluxo, bem como no final de um fluxo.

Você pode gravar informações complementares sobre o arquivo ou fluxo que não está incluído na função [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) ou [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) usando as funções [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) e [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) . Você pode registrar dados que são aplicáveis ao arquivo inteiro, como informações de direitos autorais e histórico de modificação, usando **AVIFileWriteData**. Você pode registrar informações específicas do fluxo, como configurações de compactação e descompactação, usando **AVIStreamWriteData**. As informações suplementares são armazenadas em partes separadas dentro do arquivo.

Você pode fechar o fluxo depois de concluir a gravação no novo fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Essa função limpa os buffers usados na gravação dos dados de fluxo e é concluída e fecha todas as partes de dados incompletas no arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de fluxo](stream-operations.md)
</dt> </dl>

 

 