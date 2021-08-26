---
description: Um dos principais recursos das funções na API de impressão GDI é o suporte da independência do dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Sobre a API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3aa7ea0ecfdd96237fb330868ddf2d9619aa24ee0d2f27a940c789a581a6c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951006"
---
# <a name="about-the-gdi-print-api"></a>Sobre a API de impressão GDI

Um dos principais recursos das funções na API de impressão GDI é o suporte da independência do dispositivo. Em vez de emitir comandos específicos do dispositivo para desenhar a saída em uma determinada impressora ou plotadora, um aplicativo chama funções de alto nível da interface gráfica do dispositivo (GDI). Por exemplo, para imprimir uma imagem de bitmap, um aplicativo pode chamar a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , fornecendo as coordenadas para o bitmap, bem como identificadores que identificam os DCS (contextos de dispositivo de origem e de destino). A chamada para **BitBlt** é então convertida em comandos de dispositivo bruto por um driver de impressora. Um driver de dispositivo é uma DLL (biblioteca de vínculo dinâmico) que dá suporte à DDI (interface de driver de dispositivo). Um driver de dispositivo gera comandos de dispositivo brutos quando processa chamadas para funções de DDI feitas pelo mecanismo de gráficos. Os comandos são processados pela impressora quando ele imprime a imagem. A sintaxe, o número e o tipo desses comandos variam de dispositivo para dispositivo.

Esta visão geral fornece informações sobre os tópicos a seguir.

<dl>

[Interface de impressão padrão](default-printing-interface.md)  
[Contextos de dispositivo de impressora](printer-output.md)  
[Escapes de impressora](printer-escapes.md)  
[Exibição e saída WYSIWYG](wysiwyg-display-and-output.md)  
[DEVMODE por usuário](per-user-devmode.md)  
</dl>

 

 
