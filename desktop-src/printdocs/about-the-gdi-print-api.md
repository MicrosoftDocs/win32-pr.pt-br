---
description: Um dos principais recursos das funções na API de impressão GDI é o suporte da independência do dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Sobre a API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797551"
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

 

 
