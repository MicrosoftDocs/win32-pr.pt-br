---
description: a partir do Windows XP, o painel de controle oferece suporte à categorização de itens do painel de controle. Os itens são registrados para aparecerem em uma ou mais categorias. Não é possível criar novas categorias.
title: Atribuindo categorias do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b6785a786bfe80f5a5b13bc5e9dfbe39507a2c9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478482"
---
# <a name="assigning-control-panel-categories"></a>Atribuindo categorias do painel de controle

a partir do Windows XP, o painel de controle oferece suporte à categorização de itens do painel de controle. Os itens são registrados para aparecerem em uma ou mais categorias. Não é possível criar novas categorias.

Para registrar um item do painel de controle em uma ou mais categorias, adicione valores conforme explicado na seção registro do [item do painel de controle executável](registering-control-panel-items.md) ou [registro do item do painel de controle da dll](registering-control-panel-items.md) de registro de [itens](registering-control-panel-items.md)do painel de controle, conforme apropriado.




| ID da categoria | nome da categoria (Windows 7) | nome da categoria (Windows Vista) | nome da categoria (Windows XP) | 
|-------------|---------------------------|-------------------------------|----------------------------|
| 0 | "Todos os itens do painel de controle" | "Opções adicionais"<blockquote>[!Note]<br />Qualquer item do painel de controle que não especifique uma ID de categoria aparece nessa categoria.</blockquote><br /> | "Outras opções do painel de controle"<blockquote>[!Note]<br />Qualquer item do painel de controle que não especifique uma ID de categoria aparece nessa categoria.</blockquote><br /> | 
| 1 | "Aparência e personalização" | "Aparência e personalização" | "Aparência e temas" | 
| 2 | "Hardware e som" | "Hardware e som" | "Impressoras e outros Hardwares" | 
| 3 | "Rede e Internet" | "Rede e Internet" | "Conexões de rede e Internet" | 
| 4 | Não se usa mais. Qualquer item que se adiciona somente à categoria 4 aparece na categoria 2 (hardware e som). | Não se usa mais. Qualquer item que se adiciona somente à categoria 4 aparece na categoria 2 (hardware e som). | "Sons, fala e dispositivos de áudio" | 
| 5 | "Sistema e segurança" | "Sistema e manutenção" | "Desempenho e manutenção" | 
| 6 | "Relógio, idioma e região" | "Relógio, idioma e região" | "Data, hora, idioma e opções regionais" | 
| 7 | "Facilidade de acesso" | "Facilidade de acesso" | "Opções de acessibilidade" | 
| 8 | Suplementa | Suplementa | "Adicionar ou remover programas" | 
| 9 | "Contas de usuário"<blockquote>[!Note]<br />Quando não conectado a um domínio, isso é chamado de "contas de usuário e segurança de família".</blockquote><br /> | "Contas de usuário"<blockquote>[!Note]<br />Quando não conectado a um domínio, isso é chamado de "contas de usuário e segurança de família".</blockquote><br /> | "Contas de usuário" | 
| 10 | Não se usa mais. Os itens registrados nessa categoria aparecem na categoria 5 (sistema e segurança). | “Segurança” | "Central de segurança"<blockquote>[!Note]<br />disponível somente no Windows XP Service Pack 2 (SP2) ou posterior.</blockquote><br /> | 
| 11 | Não se usa mais. Os itens registrados nessa categoria aparecem na categoria 0 (todos os itens do painel de controle). | "PC móvel"<blockquote>[!Note]<br />Essa categoria só é visível em PCs móveis.</blockquote><br /> | Não usado. | 




 

no Windows XP, as categorias **adicionam ou removem programas** e **contas de usuário** funcionam de maneira um pouco diferente de outras categorias no painel de controle. Quando um ou mais itens são adicionados a uma dessas duas categorias, o link associado no painel de controle abre uma página de categoria. Os itens registrados aparecem na parte inferior da página sob o título "ou selecionam um ícone do painel de controle". quando nenhum item é registrado para uma dessas categorias, o link associado no painel de controle chama diretamente o item de Windows padrão para essa categoria. no Windows Vista e posterior, a categoria **programas** e a categoria **contas de usuário** não têm essa propriedade.

a categoria da **central de segurança** , disponível apenas no Windows XP SP2, também é um pouco não padrão. Clicar nessa categoria abre a página **central de segurança** em uma nova janela. Os itens registrados para a **central de segurança** aparecem na parte inferior dessa página, sob o título **gerenciar configurações de segurança para:**. Clicar em um ícone abre o item do painel de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
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

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[acessando o painel de controle no modo de Cofre em Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




