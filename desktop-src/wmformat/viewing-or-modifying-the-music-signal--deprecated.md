---
title: Exibindo ou modificando o sinal de música (preterido)
description: Exibindo ou modificando o sinal de música (preterido)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- SDK do Windows Media Format, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- SDK do Windows Media Format, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- SDK do Windows Media Format, exibição ou modificação de sinal de música
- DRM (gerenciamento de direitos digitais), exibição ou modificação de sinal de música
- DRM (gerenciamento de direitos digitais), exibição ou modificação de sinal de música
- Caminho de áudio seguro da Microsoft (SAP), exibição de sinal de música ou modificação
- Caminho de áudio seguro (SAP), exibição de sinal de música ou modificação
- SAP (caminho de áudio seguro), exibição ou modificação de sinal de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783669"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a>Exibindo ou modificando o sinal de música (preterido)

Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.

No modelo de caminho de áudio seguro da Microsoft (SAP), os aplicativos não podem modificar música protegida de forma alguma. Por exemplo, quando um aplicativo tenta interceptar um sinal de música, o sinal parece ser um ruído aleatório. Como resultado, os aplicativos que normalmente modificam sinais (como um equalizador) não podem alterar o som da música.

Alguns aplicativos simplesmente exibem um sinal de música. Por exemplo, alguns aplicativos exibem luzes piscadas no tempo com o sinal de música, mas não o modificam. Para acomodar aplicativos que exibem sinais, uma pequena parte da música é descriptografada e passada em formato claro com o conteúdo criptografado. O sinal resultante é muito ruim (pior do que a qualidade do telefone), mas pode ser suficiente para aplicativos que exibem sinais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Caminho de áudio seguro da Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




