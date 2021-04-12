---
title: Introdução aos assistentes de publicação
description: O Windows XP apresenta o assistente de publicação na Web e o assistente de pedido de impressão online.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- assistentes de publicação, sobre
- Assistente de publicação na Web, sobre
- Assistente de ordenação de impressão online, sobre
- assistentes de publicação, assistente de publicação na Web
- assistentes de publicação, assistente para ordenação de impressão online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b4e6d3c515edae23d0e74f550e000bdfdfacf03
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453985"
---
# <a name="publishing-wizards-introduction"></a>Introdução aos assistentes de publicação

O Windows XP apresenta o assistente de publicação na Web e o assistente de pedido de impressão online. Com base na mesma estrutura, esses assistentes fornecem ao usuário um mecanismo simples para publicar conteúdo em um site ou para ordenar impressões feitas por meio de arquivos de imagem digital. A vantagem desses assistentes reside em sua capacidade de hospedar conteúdo HTML de provedores diferentes em suas páginas de assistente para que a aparência, o procedimento e as opções de usuário disponíveis sejam totalmente controlados pelo provedor e possam ser alterados por eles a qualquer momento sem afetar o assistente do cliente que está hospedando-os. Embora esses assistentes existentes tenham sido criados com a geração de imagens digital firmemente em mente, a estrutura e os conceitos podem ser usados para muitas outras finalidades, como um serviço de impressão de documentos ou como um método de compartilhamento de imagens com amigos e familiares.

-   [Como funciona?](#how-does-it-work)
-   [Documentação do assistente de publicação](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>Como funciona?

A experiência do usuário para o assistente de publicação na Web e o assistente de pedido de impressão online é semelhante, mas o ponto de entrada para cada assistente é diferente. Para o assistente de publicação na Web, uma tarefa intitulada **publicar esta pasta na Web** está disponível na lista de **tarefas de arquivo e pasta** à esquerda da maioria das exibições de pasta. O texto da tarefa varia de acordo com o conteúdo selecionado. Por exemplo, se um arquivo for selecionado, a tarefa lerá **publicar esse arquivo na Web** , conforme mostrado no exemplo a seguir.

![tarefas de arquivo e pasta](images/shell-pubwiz-tasks.png)

O usuário clica na tarefa para iniciar o assistente. Ao prosseguir com o assistente, o usuário receberá uma lista de provedores, conforme mostrado no exemplo a seguir. Provedores de serviços de Internet (ISPs) podem desenvolver e registrar suas próprias páginas de provedor para serem exibidas nessa lista.

![lista de provedores do assistente de publicação](images/shell-pubwiz-provs.png)

Depois que um provedor é escolhido, o assistente se conecta a esse site e a primeira página HTML é baixada para exibição no assistente. Se os usuários não tiverem uma conta com o provedor selecionado, eles terão a oportunidade de configurar um.

Várias páginas HTML estão contidas em uma única página do assistente; em outras palavras, o identificador da página de assistente que hospeda esse processamento de páginas HTML permanece constante. As páginas HTML são expostas no painel central como com qualquer página de assistente padrão. O site do provedor fornece métodos para controlar onde os botões **voltar**, **Avançar** e **Cancelar** do assistente levam enquanto as páginas HTML estão sendo exibidas. Nessas páginas HTML, os usuários podem ser solicitados a especificar uma pasta onde podem copiar arquivos ou salvar o nome de um site que desejam criar. Depois que um usuário tiver concluído todas as etapas necessárias, o site chamará um método para iniciar o carregamento, retornando o controle para o assistente. O próprio assistente manipula o upload e qualquer gráfico do atendente, como um indicador de progresso. Depois que o upload for concluído, o site do provedor poderá especificar uma URL na qual o usuário pode ir quando o assistente tiver sido fechado.

No Assistente para ordenação de impressão online, a ordem de tarefa é **impressa online** apenas em pastas de imagens, como minhas imagens, mostradas no exemplo a seguir. O processo, no entanto, é muito semelhante ao assistente de publicação na Web. O site do provedor solicita aos usuários opções como seleção de imagem, tamanhos de impressão, número de cópias e informações de pagamento.

![tarefas de imagem](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Documentação do assistente de publicação

O assistente de publicação na Web e o assistente de pedido de impressão online são discutidos em detalhes nos documentos a seguir. Também foram discutidas instruções para o desenvolvimento de aplicativos a serem hospedados por eles.

-   [Design do lado do cliente](pubwiz-client.md)
-   [Design do lado do servidor](pubwiz-server.md)
-   [Registrando um serviço](pubwiz-reg.md)
-   [Usando o manifesto de transferência](pubwiz-manifest.md)
-   [Transferir esquema de manifesto](/windows/desktop/shell/interfaces)

 

 