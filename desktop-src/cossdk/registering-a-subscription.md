---
description: Depois de registrar uma classe de evento no catálogo COM+, você pode adicionar assinantes à classe de evento e assinaturas aos assinantes.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrando uma assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370478"
---
# <a name="registering-a-subscription"></a>Registrando uma assinatura

Depois de registrar uma classe de evento no catálogo COM+, você pode adicionar assinantes à classe de evento e assinaturas aos assinantes. As assinaturas podem assinar um único método ou todos os métodos de uma interface. Para receber chamadas em mais de um método — mas não em todos os métodos — de uma interface, você deve adicionar uma assinatura para cada método para o qual deseja receber uma chamada. A ferramenta de administração de serviços de componentes pode pesquisar classes de evento registradas no catálogo COM+ que dão suporte às interfaces implementadas pelo assinante e oferece a opção de assinar. Escolha o Publicador que oferece os eventos desejados.

Para adicionar assinantes ao componente assinante, use as seguintes etapas:

1.  Depois de criar um novo aplicativo COM+ e instalar o componente de assinante, clique com o botão direito do mouse na pasta **assinaturas** para habilitar o assistente de nova assinatura do com+.

2.  Escolha a classe de evento da qual você deseja receber eventos.

3.  Insira um nome para a assinatura.

4.  Habilite a assinatura.

5.  Clique em **OK**.

Quando um aplicativo do Publicador deseja acionar um evento, o Publicador instancia o objeto da classe de evento e chama um método nele. O COM+ pesquisa o catálogo COM+ para localizar todos os assinantes. Ele cria o objeto de assinante (diretamente, na fila ou com um moniker) e passa a chamada de método originalmente feita pelo Publicador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando uma classe de evento](registering-an-event-class.md)
</dt> </dl>

 

 



