---
title: Mensagens de erro e notificações
description: Mensagens de erro e notificações
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- Macro MCIWndGetError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007444"
---
# <a name="error-messages-and-notifications"></a>Mensagens de erro e notificações

O MCIWnd usa o MCI para controlar os dispositivos que desempenham e registram dados de multimídia. Em geral, o MCIWnd exibe erros de MCI em uma caixa de diálogo de erro. Um erro MCI é gerado sempre que um comando MCI falha. Por exemplo, se seu aplicativo tentar retomar a reprodução pausada usando a macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) e o dispositivo atual não oferecer suporte a resume, um erro será relatado ao usuário.

O MCIWnd permite que você tenha duas opções para lidar com mensagens de erro:

-   Você pode impedir que mensagens de erro cheguem ao usuário. Para evitar a exibição de mensagens de erro MCI, especifique o \_ estilo de janela MCIWNDF NOERRORDLG ao criar uma instância de uma janela MCIWnd usando a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .
-   Você pode redirecioná-los para o aplicativo para exibição. Para redirecionar mensagens de erro MCI para seu aplicativo, especifique o \_ estilo de janela MCIWNDF NOTIFYERROR ao criar uma instância de uma janela MCIWnd usando **MCIWndCreate** ou **CreateWindowEx**.

Quando a notificação de erro é habilitada, o MCIWnd envia cada mensagem de notificação ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) para o manipulador de mensagens principal do pai da janela MCIWnd. Seu aplicativo deve ter um manipulador de mensagens para processar as mensagens de notificação recebidas.

Você pode obter uma descrição textual da mensagem de erro MCI mais recente usando a macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) . Essa macro retorna o texto em um buffer definido pelo aplicativo. Se a cadeia de caracteres de erro for maior que o buffer, MCIWnd truncará a cadeia de caracteres.

Você pode rotear todas as notificações para outra janela usando a macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .

 

 