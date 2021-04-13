---
description: Os controles dos pais podem ser estendidos usando as configurações e as APIs de log.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Visão geral dos recursos de extensibilidade dos controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe150c5955881b8038cdca9a1e4562ee28093f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297470"
---
# <a name="parental-controls-extensibility-features-overview"></a>Visão geral dos recursos de extensibilidade dos controles dos pais

Os controles dos pais podem ser estendidos usando as configurações e as APIs de log.

-   [Registro em log – plano de fundo](/windows)
-   [Log de extensibilidade](#logging-extensibility)
-   [Adição de link de extensibilidade da interface do usuário geral do painel de controles pais](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Substituição de filtro de conteúdo da Web](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Registro em log – plano de fundo

A Microsoft definiu vários eventos padrão para tratar de atividades comuns:

-   Sistema: os controles dos pais alteram as alterações, as alterações da conta, a alteração do relógio do sistema, as tentativas de logon com falha.
-   Usuário:
    -   Limites de sistema/tempo: tempos de logon, logout, tentativas de execução de aplicativo e duração da execução do aplicativo (consulte a observação).
    -   Restrições da Web: sites visitados e bloqueados, tentativas de download de arquivo. Navegadores da Web e aplicativos do tipo navegador não precisam fazer logon, pois o LSP de filtro de conteúdo da Web faz isso. Os filtros da Web de substituição precisariam gerar esses eventos.
    -   Jogos: jogos reproduzidos e bloqueados, ponta de jogo (eventos juntos fornecem duração reproduzida).
    -   Permitir e bloquear programas específicos: tentativa de execução, desligamento, bloqueado por restrições gerais de aplicativo.
    -   Mensagens instantâneas: tentativa de inicialização de conversão, tentativa de junção de conversa, licença de conversa, vídeo/áudio/jogo/serviço de mensagem curta/transferência de arquivo/recurso de permuta de URL, tentativa de alteração da lista de contatos.
    -   Email: recebimento ou recebimento bloqueado, tentativa de envio, tentativa de alteração da lista de contatos.
    -   Mídia: mídia reproduzida e tentada.

Nem todos os eventos anteriores são adequados para uso por aplicativos. As alterações de conta, a alteração do relógio do sistema e o log de eventos de logon e logoff são implementadas somente pelo sistema operacional e, portanto, não são expostas publicamente.

> [!Note]  
> A instrumentação de eventos de entrada e saída do aplicativo está disponível no Windows Vista e é configurada pelos controles dos pais para registrar esses dados.

 

## <a name="logging-extensibility"></a>Log de extensibilidade

Um evento personalizado genérico também é definido com 3 marcas/valores disponíveis para que os ISVs geralmente não precisem definir seus próprios em um manifesto. O Visualizador de log reconhecerá e exibirá os valores e cabeçalhos de marca se o número de campos usados (1 a 3) e os títulos de cada campo forem registrados usando a API WMI. O Visualizador de Eventos genérico também pode ser usado para exibir eventos personalizados.

Se o evento personalizado genérico não for adequado, um ISV poderá definir seu próprio usando um manifesto do aplicativo e poderá registrar cabeçalhos para até três campos usando a mesma API do WMI.

Os ISVs podem optar por definir seus próprios eventos e consumi-los independentemente do Visualizador de log por meio de APIs públicas do Windows. Isso não tem o benefício da centralização de log completa.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Adição de link de extensibilidade da interface do usuário geral do painel de controles pais

Um link de extensibilidade da interface do usuário de uso geral é exposto acessando as configurações por meio do WMI, criando uma instância de extensão do caminho de DLL de recurso de nome e ID, caminho de imagem (bitmap), caminho de imagem de estado desabilitado (bitmap), caminho de DLL de recurso de subtítulo e ID e especificações de caminho executável. Depois de registrado, o link será exibido na área mais configurações do painel de controles dos pais e clicar nele invocará o executável especificado.

A cadeia de caracteres do caminho executável pode, opcionalmente, incluir um token para que o SID do usuário atual seja substituído antes da invocação. Isso permite que a execução do link opere no contexto do usuário para o qual a página de Hub está sendo exibida no momento, se o executável precisar saber o SID.

## <a name="web-content-filter-replacement"></a>Substituição de filtro de conteúdo da Web

Conforme observado no tópico, os [controles dos pais In-Box restrições e interfaces do usuário](parental-controls-in-box-restrictions-and-user-interfaces.md), o filtro de conteúdo da Web na caixa pode ser substituído por um filtro fornecido pelo fornecedor. Isso é realizado acessando as configurações por meio do WMI para definir um GUID e um nome proprietário da filtragem.

O mecanismo geral de extensibilidade da interface do usuário é usado para expor um filtro de terceiros. Esse é o mesmo mecanismo usado para qualquer extensão que deseja aparecer na seção mais configurações do painel de controle pai de nível superior. Fazer a etapa adicional de definir o mesmo GUID e um caminho de DLL de recurso de nome apropriado e uma ID para as configurações de filtro no nível do sistema fará com que o link de filtro exibido na caixa seja ocultado e a entrada de terceiros seja mostrada na parte superior da seção mais configurações. O nome registrado para o filtro será mostrado na seção de resumo.

Redefinir o GUID do filtro e as configurações do caminho/ID do nome resultará no filtro de conteúdo da Web na caixa, restabelecendo a si mesmo como o filtro ativo e aparecendo novamente na seção Configurações do Windows.

Observe que os filtros de terceiros não são restritos nas tecnologias usadas para conectar-se ao Windows Communications. Um filtro deve expor apenas suas configurações usando um link de extensibilidade e honrar as configurações de controles pais adequadas.

 

 
