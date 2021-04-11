---
title: Métodos IPaperSink
description: O copaper expõe a interface IConnectionPointContainer para que os clientes possam se conectar ao copaper a fim de receber notificações de eventos especificados que ocorrem em copapel.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8dee615b278c5214ad1efa3c10d22759620103
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162364"
---
# <a name="ipapersink-methods"></a>Métodos IPaperSink

O copaper expõe a interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) para que os clientes possam se conectar ao copaper a fim de receber notificações de eventos especificados que ocorrem em copapel. Ao expor essa interface, o copaper se torna um objeto conectável. Um cliente pode chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para essa interface e usá-la para obter os pontos de conexão do objeto. A participação do cliente neste esquema é abordada no exemplo de **StoClien** associado.

Basicamente, o cliente implementa o que é chamado de coletor na forma de um objeto de coletor com uma interface de coletor. A interface do coletor recebe chamadas de notificação de eventos de saída do copaper após o coletor ser corretamente conectado pelo cliente a uma instância de copapel. O cliente faz a conexão usando um objeto de ponto de conexão que é gerenciado por copaper. Pode haver inúmeros pontos de conexão em um único objeto COM conectável. No exemplo de **StoServe** , o copaper tem apenas um ponto de conexão, que manipula os eventos de papel de desenho.

Qualquer número de clientes pode se conectar a um único ponto de conexão. O ponto de conexão do CONNPOINT \_ PAPERSINK no copaper mantém um grupo de conexões que podem crescer dinamicamente no tempo de execução. Os detalhes completos sobre o suporte a objetos conectáveis do copaper são codificados em arquivos CONNECT. H e conectar. CPP e não serão abordados aqui. A construção é muito semelhante ao que foi estudado no exemplo de código para conservar.

O cliente **StoClien** implementa os objetos de coletor apropriados para os pontos de conexão que espera encontrar no copaper. No contexto de copaper, o objeto de coletor importante que o **StoClien** implementa expõe a interface **IPaperSink** . Essa é a interface de saída usada pelo copaper para notificar **StoClien** de vários eventos em copapel.

Aqui está um resumo dos métodos no **IPaperSink** do IPAPER. H no \\ diretório irmão Inc.



| Método   | Descrição                                                   |
|----------|---------------------------------------------------------------|
| Bloqueado   | Um cliente assumiu o controle e bloqueou o documento.           |
| Desbloqueado | Um cliente abandonou o controle do papel.               |
| Carregado   | Um cliente carregou o conteúdo de papel de seu próprio arquivo composto. |
| Salvo    | Um cliente salvou o conteúdo de papel em seu próprio arquivo composto.    |
| InkStart | Um cliente iniciou uma sequência de desenho de tinta colorida para o documento.   |
| InkDraw  | Um cliente está colocando pontos de dados de tinta na superfície do papel.     |
| InkStop  | Um cliente interrompeu sua sequência de desenho de tinta para o documento.   |
| Apagados   | Um cliente apagou todos os dados de tinta do documento.              |
| Redimensionado  | Um cliente redimensionou o documento.                               |



 

Esses métodos são amplamente auto-explicativos. Embora o coletor deva implementar todos esses métodos de alguma maneira, muitos são implementados como stubs e não são usados nos exemplos de StoClien de **StoServe** /  .

Um método importante usado nesses exemplos é o método carregado. Quando o copapel é informado pelo cliente para carregar um novo desenho do arquivo, ele precisa de uma maneira de notificar o cliente quando os novos dados são carregados. Para fazer isso, o copaper chama **IPaperSink:: Loaded** no coletor do cliente. O cliente pode então chamar [**IPaper:: redesenhar**](ipaper--redraw.md) para solicitar que o copapel reproduza os novos dados para o cliente. Redesenhar faz com que o desenho carregado na exibição do cliente seja redesenhado. Quando a carga é concluída, o desenho carregado recentemente é exibido automaticamente na janela fornecida pelo cliente.

Consulte [**IPaper:: redesenhar**](ipaper--redraw.md) para obter informações completas sobre a conectividade desse método IPaper com o **IPaperSink**.

Os  métodos IPaperSink **InkStart**, **InkDraw** e **InkStop** são usados para enviar pacotes de dados de tinta individuais de volta para o cliente. Na recepção, o cliente os pinta em sua exibição da mesma maneira como quando as enviou originalmente para o copapel. A lógica acima é geral o suficiente para permitir que vários clientes que estão escutando no mesmo ponto de conexão do CONNPOINT \_ PAPERSINK. Se uma instância de copapel comum foi compartilhada por esses clientes, todas elas podem exibir o mesmo desenho conectando-se a esse ponto de conexão.

 

 