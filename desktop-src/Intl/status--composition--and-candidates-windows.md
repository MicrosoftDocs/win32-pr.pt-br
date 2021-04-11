---
description: As janelas status, composição e candidatos formam a interface do usuário para o IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Janelas de status, composição e candidatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b800def67299a464fd232a08a2bbff0a2a60a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172031"
---
# <a name="status-composition-and-candidates-windows"></a>Janelas de status, composição e candidatos

As janelas status, composição e candidatos formam a interface do usuário para o IME. A janela de status indica que o IME está aberto e fornece ao usuário os meios para definir os modos de conversão. A janela composição é exibida quando o usuário digita o texto e, dependendo do modo de conversão, exibe o texto como inserido ou exibe o texto convertido. A janela candidatos aparece em conjunto com a janela composição. Ele contém uma lista de "candidatos" (caracteres alternativos) para o caractere ou caracteres selecionados na janela de composição. O usuário pode rolar a lista de candidatos e selecionar os caracteres desejados e retornar à janela de composição. O usuário pode compor o texto desejado dessa maneira até que a cadeia de caracteres de composição seja finalizada e a janela seja fechada.

O IME envia os caracteres compostos para o aplicativo com reconhecimento de IME na forma de mensagens de resultado do [**WM \_ IME \_ Char**](wm-ime-char.md) ou do [**WM \_ IME \_**](wm-ime-composition.md)/GCS \_ . Se o aplicativo não processar essas mensagens, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) as converterá em uma ou mais mensagens do [**WM \_ Char**](../inputdev/wm-char.md) .

Por padrão, o sistema operacional cria e gerencia automaticamente as janelas de status, composição e candidatos para os requisitos de entrada de texto. Para muitos aplicativos, esse processamento padrão é suficiente. Esses aplicativos dependem inteiramente do sistema operacional para o suporte do IME e são considerados "inconscientes", pois não sabem das muitas tarefas que o sistema operacional realiza para gerenciar as janelas do IME.

Um aplicativo com reconhecimento de IME, por outro lado, participa da criação e do gerenciamento das janelas do IME. Esses aplicativos controlam a operação, a posição e a aparência das janelas padrão, enviando mensagens para essas janelas e interceptando e processando mensagens das janelas. Em alguns casos, os aplicativos criam suas próprias janelas de IME e fornecem processamento completo para suas janelas de status, composição e candidatos personalizadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
