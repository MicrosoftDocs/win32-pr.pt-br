---
title: Sobre controles de endereço IP
description: Um controle de endereço IP (Internet Protocol) permite que o usuário insira um endereço IP em um formato facilmente compreendido.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917709"
---
# <a name="about-ip-address-controls"></a>Sobre controles de endereço IP

Um controle de endereço IP (Internet Protocol) permite que o usuário insira um endereço IP em um formato facilmente compreendido. Esse controle também permite que o aplicativo obtenha o endereço em formato numérico em vez de em formato de texto.

-   [Sobre controles de endereço IP](#about-ip-address-controls)
-   [Criando um controle de endereço IP](#creating-an-ip-address-control)
-   [Um controle de endereço IP é um controle de edição?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Sobre controles de endereço IP

O Windows Internet Explorer versão 4,0 apresenta o controle de endereço IP, um novo controle semelhante a um controle de edição que permite ao usuário inserir um endereço numérico no formato de protocolo IP. Esse formato consiste em campos de 4 3 dígitos. Cada campo é tratado individualmente; os números de campo são baseados em zero e passam da esquerda para a direita, conforme mostrado nesta figura.

![diagrama mostrando valores em cada um dos quatro campos de um controle de endereço IP](images/ipa-scrn.png)

O controle permite que apenas texto numérico seja inserido em cada um dos campos. Depois que três dígitos forem inseridos em um determinado campo, o foco do teclado será movido automaticamente para o próximo campo. Se o preenchimento do campo inteiro não for exigido pelo aplicativo, o usuário poderá inserir menos de três dígitos. Por exemplo, se o campo deve conter apenas o número vinte e um, digitando "21" e pressionar a tecla, o usuário será levado para o próximo campo.

O intervalo padrão para cada campo é de 0 a 255, mas o aplicativo pode definir o intervalo para quaisquer valores entre esses limites com a mensagem [**IPM \_ SETRANGE**](ipm-setrange.md) .

> [!Note]  
> O controle de endereço IP é implementado na versão 4,71 e posterior do Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Criando um controle de endereço IP

Antes de criar um controle de endereço IP, chame [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) com o sinalizador de **\_ \_ classes de Internet ICC** definido no membro **dwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

Use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de endereço IP. O nome da classe para o controle é [**WC \_ IPAddress**](common-control-window-classes.md), que é definido em commctrl. h. Não existe nenhum estilo específico de controle de endereço IP; no entanto, como esse é um controle filho, use o estilo [**\_ filho WS**](/windows/desktop/winmsg/window-styles) como um mínimo.

## <a name="is-an-ip-address-control-an-edit-control"></a>Um controle de endereço IP é um controle de edição?

Um controle de endereço IP não é um controle de edição e não responderá a \_ mensagens em. No entanto, ele enviará à janela do proprietário as notificações de controle de edição a seguir por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . Observe que o controle de endereço IP também enviará notificações IPN particulares \_ por meio da mensagem de [**\_ notificação do WM**](wm-notify.md) .



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Notificação**                  | **Motivo da notificação**                                                                                                                                                                             |
| [EN \_ SETFOCUS](en-setfocus.md)   | Enviado quando o controle de endereço IP Obtém o foco do teclado.                                                                                                                                              |
| [KILLFOCUS de EN \_](en-killfocus.md) | Enviado quando o controle de endereço IP perde o foco do teclado.                                                                                                                                              |
| [alteração de EN \_](en-change.md)       | Enviado quando qualquer campo no controle de endereço IP é alterado. Assim como a notificação de [ \_ alteração en](en-change.md) de um controle de edição padrão, essa notificação é recebida depois que a tela é atualizada. |



 

 

 