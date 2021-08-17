---
title: Sobre controles de endereço IP
description: Um controle de endereço IP (Protocolo IP) permite que o usuário insira um endereço IP em um formato facilmente compreendido.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce537b3b3a92846961e95321889d106a61a81e14bfa4cbc4edd93da5c8c033ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435586"
---
# <a name="about-ip-address-controls"></a>Sobre controles de endereço IP

Um controle de endereço IP (Protocolo IP) permite que o usuário insira um endereço IP em um formato facilmente compreendido. Esse controle também permite que o aplicativo obtenha o endereço em formato numérico em vez de em formato de texto.

-   [Sobre controles de endereço IP](#about-ip-address-controls)
-   [Criando um controle de endereço IP](#creating-an-ip-address-control)
-   [Um controle de endereço IP é um controle de edição?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Sobre controles de endereço IP

Windows Internet Explorer versão 4.0 introduz o controle de endereço IP, um novo controle semelhante a um controle de edição que permite que o usuário insira um endereço numérico no formato ip (protocolo IP). Esse formato consiste em quatro campos de três dígitos. Cada campo é tratado individualmente; os números de campo são baseados em zero e vão da esquerda para a direita, conforme mostrado nesta figura.

![diagrama mostrando valores em cada um dos quatro campos de um controle de endereço IP](images/ipa-scrn.png)

O controle permite que apenas texto numérico seja inserido em cada um dos campos. Depois que três dígitos são inseridos em um determinado campo, o foco do teclado é movido automaticamente para o próximo campo. Se o preenchimento de todo o campo não for exigido pelo aplicativo, o usuário poderá inserir menos de três dígitos. Por exemplo, se o campo deve conter apenas o número 21, digitar "21" e pressionar a tecla levará o usuário para o próximo campo.

O intervalo padrão para cada campo é de 0 a 255, mas o aplicativo pode definir o intervalo para qualquer valor entre esses limites com a mensagem [**\_ SETRANGE do IPM.**](ipm-setrange.md)

> [!Note]  
> O controle de endereço IP é implementado na versão 4.71 e posterior do Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Criando um controle de endereço IP

Antes de criar um controle de endereço IP, chame [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) com o sinalizador **ICC \_ INTERNET \_ CLASSES** definido no membro **dwICC** da estrutura [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)

Use a [**função CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de endereço IP. O nome da classe para o controle [**é WC \_ IPADDRESS,**](common-control-window-classes.md)que é definido em Commctrl.h. Não existem estilos específicos do controle de endereço IP; no entanto, como esse é um controle filho, use o [**estilo FILHO do WS \_**](/windows/desktop/winmsg/window-styles) como um mínimo.

## <a name="is-an-ip-address-control-an-edit-control"></a>Um controle de endereço IP é um controle de edição?

Um controle de endereço IP não é um controle de edição e não responderá a mensagens \_ EM. No entanto, ele enviará à janela do proprietário as seguintes notificações de controle de edição por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) Observe que o controle de endereço IP também enviará notificações de IPN privado \_ por meio da mensagem WM [**\_ NOTIFY.**](wm-notify.md)



|     Notificação                              |     Motivo da notificação                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EN \_ SETFOCUS](en-setfocus.md)   | Enviado quando o controle de endereço IP obtém o foco do teclado.                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | Enviado quando o controle de endereço IP perde o foco do teclado.                                                                                                                                              |
| [EN \_ CHANGE](en-change.md)       | Enviado quando qualquer campo no controle de endereço IP muda. Como a [ \_ notificação EN CHANGE](en-change.md) de um controle de edição padrão, essa notificação é recebida após a atualização da tela. |



 

 

 