---
title: Adicionando User-Controlled reprodução
description: Adicionando User-Controlled reprodução
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105752629"
---
# <a name="adding-user-controlled-playback"></a>Adicionando User-Controlled reprodução

Você pode adicionar a reprodução controlada pelo usuário a um aplicativo existente chamando a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) da seguinte maneira:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Os parâmetros [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identificam identificadores para a janela pai e para a instância de módulo associada à janela MCIWnd. Eles também especificam estilos de janela e o nome de arquivo (ou nome do dispositivo) a ser associado à janela MCIWnd.

O **MCIWndCreate** executa automaticamente as seguintes etapas que, para outras classes de janela, você pode implementar em seu código por conta própria:

1.  Registre a classe da janela MCIWnd.
2.  Crie a janela MCIWnd.
3.  Carregar o conteúdo especificado.
4.  Estabeleça a posição de reprodução atual no início do conteúdo.
5.  Exibir o controle de dispositivo.
6.  Exiba a área de reprodução da janela, se necessário.

 

 




