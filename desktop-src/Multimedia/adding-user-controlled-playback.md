---
title: Adicionando User-Controlled reprodução
description: Adicionando User-Controlled reprodução
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62d4e4af43be9877ec5bf3fae452e44ae415bc47047448cb65b64ad3446e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941814"
---
# <a name="adding-user-controlled-playback"></a>Adicionando User-Controlled reprodução

Você pode adicionar reprodução controlada pelo usuário a um aplicativo existente chamando a [**função MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) da seguinte forma:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Os [**parâmetros MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identificam identificador para a janela pai e para a instância do módulo associada à janela MCIWnd. Eles também especificam estilos de janela e o nome do arquivo (ou nome do dispositivo) a ser associado à janela MCIWnd.

**O MCIWndCreate** executa automaticamente as seguintes etapas que, para outras classes de janela, você mesmo implementaria em seu código:

1.  Registre a classe de janela MCIWnd.
2.  Crie a janela MCIWnd.
3.  Carregue o conteúdo especificado.
4.  Estabeleça a posição de reprodução atual no início do conteúdo.
5.  Exibir o controle de dispositivo.
6.  Exibir a área de reprodução da janela, se necessário.

 

 




