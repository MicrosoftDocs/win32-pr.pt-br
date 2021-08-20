---
title: Métodos IPaperSink
description: O COPaper expõe a interface IConnectionPointContainer para que os clientes possam se conectar ao COPaper para receber notificações de eventos especificados que ocorrem no COPaper.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf83c3b4bb5c043b02e05324521ea2a4e5783fe4ef959487d83a2607851b533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961346"
---
# <a name="ipapersink-methods"></a>Métodos IPaperSink

O COPaper expõe a interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) para que os clientes possam se conectar ao COPaper para receber notificações de eventos especificados que ocorrem no COPaper. Ao expor essa interface, o COPaper se torna um objeto conectável. Um cliente pode chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para essa interface e usá-la para obter os pontos de conexão do objeto. A participação do cliente nesse esquema é abordada no exemplo **de StoClhin** associado.

Basicamente, o cliente implementa o que é chamado de um sink na forma de um objeto de sink com uma interface de sink. A interface do sink recebe chamadas de notificação de eventos de saída do COPaper depois que o sink é conectado corretamente pelo cliente a uma instância do COPaper. O cliente faz a conexão usando um objeto de ponto de conexão gerenciado pelo COPaper. Pode haver vários pontos de conexão em um único objeto COM conectável. No exemplo **de StoServe,** COPaper tem apenas um ponto de conexão, que lida com eventos de papel de desenho.

Qualquer número de clientes pode se conectar a um único ponto de conexão. O ponto de conexão CONNPOINT PAPERSINK no COPaper mantém um grupo de conexões que podem crescer \_ dinamicamente em tempo de operação. Os detalhes completos sobre o suporte ao objeto conectável do COPaper são codificados nos arquivos CONNECT. H e CONNECT. CPP e não serão abordados aqui. A construção é muito semelhante ao que foi estudou no exemplo de código CONSERVE.

O **cliente StoCl ltda** implementa objetos de sink apropriados para os pontos de conexão que ele espera encontrar no COPaper. No contexto do COPaper, o objeto de sink importante que **o StoCl euclid** implementa expõe a interface **IPaperSink.** Essa é a interface de saída usada pelo COPaper para notificar **StoCl ltda** de vários eventos no COPaper.

Aqui está um resumo dos métodos em **IPaperSink** de IPAPER. H no diretório \\ irmão inc.



| Método   | Descrição                                                   |
|----------|---------------------------------------------------------------|
| Bloqueado   | Um cliente passou a controlar e travada o papel.           |
| Desbloqueado | Um cliente relinquisou o controle do papel.               |
| Carregado   | Um cliente carregou o conteúdo de papel de seu próprio arquivo composto. |
| Salvo    | Um cliente salvou o conteúdo de papel em seu próprio arquivo composto.    |
| InkStart | Um cliente iniciou uma sequência de desenho de tinta colorida para o papel.   |
| InkDraw  | Um cliente está colocando pontos de dados de tinta na superfície de papel.     |
| InkStop  | Um cliente interrompeu sua sequência de desenho de tinta para o papel.   |
| Apagado   | Um cliente a apagará todos os dados de tinta do papel.              |
| Redimensionado  | Um cliente reeslizou o papel.                               |



 

Esses métodos são amplamente autoexplicativos. Embora o sink deve implementar todos esses métodos de alguma forma, muitos são implementados como stubs e não são usados nos exemplos **StoServe** / **StoClhin.**

Um método importante usado nesses exemplos é o método Loaded. Quando o COPaper é informado pelo cliente para carregar um novo desenho do arquivo, ele precisa de uma maneira de notificar o cliente quando os novos dados são carregados. Para fazer isso, o COPaper chama **IPaperSink::Loaded** no sink do cliente. Em seguida, o cliente pode [**chamar IPaper::Redraw**](ipaper--redraw.md) para solicitar que o COPaper reproduza os novos dados para o cliente. Redesenhar faz com que o desenho carregado na exibição do cliente seja repintado. Quando a carga é concluída, o desenho recém-carregado é exibido automaticamente na janela fornecida pelo cliente.

Consulte [**IPaper::Redraw**](ipaper--redraw.md) para obter informações completas sobre a conectividade desse método IPaper com **IPaperSink.**

Os **métodos IPaperSink** **InkStart,** **InkDraw** e **InkStop** são usados para enviar pacotes de dados de tinta individuais de volta para o cliente. Na recepção, o cliente pinta-os em sua exibição da mesma maneira que quando originalmente os enviou ao COPaper. A lógica acima é geral o suficiente para permitir vários clientes que estão todos escutando no mesmo ponto de conexão CONNPOINT \_ PAPERSINK. Se uma instância de COPaper comum tiver sido compartilhada por esses clientes, todos eles poderão exibir o mesmo desenho conectando-se a esse ponto de conexão.

 

 