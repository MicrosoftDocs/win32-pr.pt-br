---
description: A partir do Windows XP, o painel de controle oferece suporte à categorização de itens do painel de controle. Os itens são registrados para aparecerem em uma ou mais categorias. Não é possível criar novas categorias.
title: Atribuindo categorias do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967364"
---
# <a name="assigning-control-panel-categories"></a>Atribuindo categorias do painel de controle

A partir do Windows XP, o painel de controle oferece suporte à categorização de itens do painel de controle. Os itens são registrados para aparecerem em uma ou mais categorias. Não é possível criar novas categorias.

Para registrar um item do painel de controle em uma ou mais categorias, adicione valores conforme explicado na seção registro do [item do painel de controle executável](registering-control-panel-items.md) ou [registro do item do painel de controle da dll](registering-control-panel-items.md) de registro de [itens](registering-control-panel-items.md)do painel de controle, conforme apropriado.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>ID da categoria</th>
<th>Nome da categoria (Windows 7)</th>
<th>Nome da categoria (Windows Vista)</th>
<th>Nome da categoria (Windows XP)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>&quot;Todos os itens do painel de controle&quot;</td>
<td>&quot;Opções adicionais&quot;
<blockquote>
[!Note]<br />
Qualquer item do painel de controle que não especifique uma ID de categoria aparece nessa categoria.
</blockquote>
<br/></td>
<td>&quot;Outras opções do painel de controle&quot;
<blockquote>
[!Note]<br />
Qualquer item do painel de controle que não especifique uma ID de categoria aparece nessa categoria.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>1</td>
<td>&quot;Aparência e Personalização&quot;</td>
<td>&quot;Aparência e Personalização&quot;</td>
<td>&quot;Aparência e temas&quot;</td>
</tr>
<tr class="odd">
<td>2</td>
<td>&quot;Hardware e som&quot;</td>
<td>&quot;Hardware e som&quot;</td>
<td>&quot;Impressoras e outros tipos de hardware&quot;</td>
</tr>
<tr class="even">
<td>3</td>
<td>&quot;Rede e Internet&quot;</td>
<td>&quot;Rede e Internet&quot;</td>
<td>&quot;Conexões de rede e Internet&quot;</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Não se usa mais. Qualquer item que se adiciona somente à categoria 4 aparece na categoria 2 (hardware e som).</td>
<td>Não se usa mais. Qualquer item que se adiciona somente à categoria 4 aparece na categoria 2 (hardware e som).</td>
<td>&quot;Sons, fala e dispositivos de áudio&quot;</td>
</tr>
<tr class="even">
<td>5</td>
<td>&quot;Sistema e segurança&quot;</td>
<td>&quot;Sistema e manutenção&quot;</td>
<td>&quot;Desempenho e manutenção&quot;</td>
</tr>
<tr class="odd">
<td>6</td>
<td>&quot;Relógio, idioma e região&quot;</td>
<td>&quot;Relógio, idioma e região&quot;</td>
<td>&quot;Opções de data, hora, idioma e regionais&quot;</td>
</tr>
<tr class="even">
<td>7</td>
<td>&quot;Facilidade de Acesso&quot;</td>
<td>&quot;Facilidade de Acesso&quot;</td>
<td>&quot;Opções de acessibilidade&quot;</td>
</tr>
<tr class="odd">
<td>8</td>
<td>&quot;Programas&quot;</td>
<td>&quot;Programas&quot;</td>
<td>&quot;Adicionar ou remover programas&quot;</td>
</tr>
<tr class="even">
<td>9</td>
<td>&quot;Contas de Usuário&quot;
<blockquote>
[!Note]<br />
Quando não conectado a um domínio, isso é chamado de &quot; contas de usuário e segurança de família &quot; .
</blockquote>
<br/></td>
<td>&quot;Contas de Usuário&quot;
<blockquote>
[!Note]<br />
Quando não conectado a um domínio, isso é chamado de &quot; contas de usuário e segurança de família &quot; .
</blockquote>
<br/></td>
<td>&quot;Contas de Usuário&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Não se usa mais. Os itens registrados nessa categoria aparecem na categoria 5 (sistema e segurança).</td>
<td>&quot;Segurança&quot;</td>
<td>&quot;Central de Segurança&quot;
<blockquote>
[!Note]<br />
Disponível apenas no Windows XP Service Pack 2 (SP2) ou posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>Não se usa mais. Os itens registrados nessa categoria aparecem na categoria 0 (todos os itens do painel de controle).</td>
<td>&quot;PC móvel&quot;
<blockquote>
[!Note]<br />
Essa categoria só é visível em PCs móveis.
</blockquote>
<br/></td>
<td>Não usado.</td>
</tr>
</tbody>
</table>



 

No Windows XP, as categorias **adicionam ou removem programas** e **contas de usuário** funcionam de maneira um pouco diferente de outras categorias no painel de controle. Quando um ou mais itens são adicionados a uma dessas duas categorias, o link associado no painel de controle abre uma página de categoria. Os itens registrados aparecem na parte inferior da página sob o título "ou selecionam um ícone do painel de controle". Quando nenhum item é registrado para uma dessas categorias, o link associado no painel de controle chama diretamente o item padrão do Windows para essa categoria. No Windows Vista e posterior, a categoria **programas** e a categoria **contas de usuário** não têm essa propriedade.

A categoria da **central de segurança** , disponível apenas no Windows XP SP2, também é um pouco não padrão. Clicar nessa categoria abre a página **central de segurança** em uma nova janela. Os itens registrados para a **central de segurança** aparecem na parte inferior dessa página, sob o título **gerenciar configurações de segurança para:**. Clicar em um ícone abre o item do painel de controle.

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

[Acessando o painel de controle no modo de segurança no Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




