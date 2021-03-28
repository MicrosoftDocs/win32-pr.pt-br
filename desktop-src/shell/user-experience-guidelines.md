---
description: A principal responsabilidade de qualquer item do painel de controle é exibir uma janela que permite ao usuário exibir e manipular as configurações.
title: Diretrizes da Experiência do Usuário
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989088"
---
# <a name="user-experience-guidelines"></a>Diretrizes da Experiência do Usuário

A principal responsabilidade de qualquer item do painel de controle é exibir uma janela que permite ao usuário exibir e manipular as configurações. Consulte as [diretrizes UX (experiência do usuário dos painéis de controle)](../uxguide/winenv-ctrl-panels.md) para o comportamento e o design de itens do painel de controle. As diretrizes discutidas neste tópico mostram um método de fluxo de tarefas de organizar um item do painel de controle. Isso coloca as configurações mais importantes em um home page. As configurações usadas com menos frequência são colocadas em páginas spoke ou acessadas de links em um painel lateral.

O painel de controle inclui muitos itens que seguem essas diretrizes, como a facilidade de central de acesso e a central de rede e compartilhamento. Outros itens do painel de controle usam o formato de folha de propriedades da caixa de diálogo com guias, como nas versões anteriores do Windows. Os exemplos incluem o item do mouse e as opções da Internet. O uso do formato de folha de propriedades deve ser descontinuado. Se você criar novos itens do painel de controle, siga as diretrizes de fluxo de tarefas.

No passado, os itens do painel de controle eram empacotados como arquivos. cpl. Isso não é mais necessário. Novos itens do painel de controle devem ser implementados como um arquivo. exe autônomo ou como uma opção de sinalizador de linha de comando para o arquivo executável principal do aplicativo.

> [!Note]  
> Em sistemas de 64 bits, os itens do painel de controle de 32 bits são exibidos no painel de controle quando a opção de **pasta exibir itens do painel de controle de 32 bits** está selecionada. Os itens de 32 bits devem estar localizados na pasta% SystemRoot% \\ SysWOW64 a ser exibida. Eles não exigem nenhum registro adicional.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Processamento de mensagens do painel de controle](message-processing.md)
</dt> <dt>

[Executando itens do painel de controle](executing-control-panel-items.md)
</dt> <dt>

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o painel de controle no modo de segurança](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



