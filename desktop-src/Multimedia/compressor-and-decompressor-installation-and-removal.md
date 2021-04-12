---
title: Instalação e remoção de compactador e descompactador
description: Instalação e remoção de compactador e descompactador
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- VCM (Gerenciador de compactação de vídeo), instalando os compactadores
- VCM (Gerenciador de compactação de vídeo), instalando os compactadores
- Função ICInstall
- Função ICRemove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293917"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Instalação e remoção de compactador e descompactador

Um aplicativo pode usar compactadores e descompactadores que já estão instalados em um sistema que executa o sistema operacional Microsoft Windows. Um aplicativo também pode instalar compactadores e descompactadores para usos gerais ou especiais. A maioria dos aplicativos não precisará instalar ou remover os compactadores ou os decompactdores, pois eles geralmente são instalados por um programa de instalação. No entanto, um aplicativo pode instalar um compactador diretamente ou instalar uma função como um compressor.

Um aplicativo pode instalar um compressor ou descompactador (ou uma função usada como um compactador ou descompactador) usando a função [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) . Essa função cria uma entrada no registro que identifica o compressor ou o descompactador. Seu aplicativo ou outro aplicativo pode pesquisar o registro para determinar se o sistema contém um compressor ou descompactador adequado para seus dados. Use **ICInstall** para instalar todos os drivers de compactação e descompactação.

Um aplicativo pode localizar e abrir um compactador ou descompactador instalado usando as funções [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Quando um aplicativo termina de usar um compressor ou um descompactador, ele o fecha usando a função [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) .

Um aplicativo pode remover a entrada do registro para um compactador ou descompactador instalado usando a função [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove) . Essa função remove a entrada do registro de um compressor ou descompactador que não está carregado atualmente na memória.

Um aplicativo pode restringir o uso de um compressor ou descompactar instalando, abrindo, fechando-o e removendo-o.

Como alternativa, para usar uma função internamente como um compressor ou um descompactador sem instalá-lo no registro, um aplicativo pode usar a função [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) . Essa função requer que o aplicativo de chamada tenha o endereço da função a ser usado como um compactador ou descompactador. Quando o aplicativo termina de usar a função, ele deve fechá-lo usando **ICClose**. Como a função não foi instalada, o aplicativo não precisa remover a função do registro.

A estrutura interna de uma função usada como um compressor ou descompactador deve ser a mesma que a função de ponto de entrada [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) usada por drivers instaláveis. Para obter mais informações sobre a função de ponto de entrada do **DriverProc** , consulte [drivers instaláveis](installable-drivers.md).

> [!Note]  
> Um aplicativo que instala uma função como um compactador ou descompactador deve remover a função antes que o aplicativo seja fechado para que outros aplicativos não tentem usar a função. Ao remover uma função, o aplicativo deve identificá-la com o código de quatro caracteres usado para instalá-la.

 

 

 