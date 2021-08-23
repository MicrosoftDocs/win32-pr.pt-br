---
description: A partir Windows XP, o Painel de Controle dá suporte à categorização de Painel de Controle itens. Os itens são registrados para aparecer em uma ou mais categorias. Novas categorias não podem ser criadas.
title: Atribuindo Painel de Controle categorias
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0d70854177baecf6261d550bc5ad37cf5319eed323ae9b17f5fd281118acd8b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593626"
---
# <a name="assigning-control-panel-categories"></a>Atribuindo Painel de Controle categorias

A partir Windows XP, o Painel de Controle dá suporte à categorização de Painel de Controle itens. Os itens são registrados para aparecer em uma ou mais categorias. Novas categorias não podem ser criadas.

Para registrar um item Painel de Controle em uma ou mais categorias, adicione valores, conforme explicado na seção Registro de [Item](registering-control-panel-items.md) Painel de Controle Executável ou Registro de Item [Painel de Controle DLL](registering-control-panel-items.md) de Registrando [itens Painel de Controle](registering-control-panel-items.md), conforme apropriado.



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
<td>&quot;Todos os Painel de Controle itens&quot;</td>
<td>&quot;Opções adicionais&quot;
<blockquote>
[!Note]<br />
Qualquer Painel de Controle item que não especifica uma ID de categoria é exibido nesta categoria.
</blockquote>
<br/></td>
<td>&quot;Outras Painel de Controle opções&quot;
<blockquote>
[!Note]<br />
Qualquer Painel de Controle item que não especifica uma ID de categoria é exibido nesta categoria.
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
<td>&quot;Impressoras e outros hardwares&quot;</td>
</tr>
<tr class="even">
<td>3</td>
<td>&quot;Rede e Internet&quot;</td>
<td>&quot;Rede e Internet&quot;</td>
<td>&quot;Conexões de Rede e Internet&quot;</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Não se usa mais. Qualquer item que se adiciona apenas à categoria 4 aparece na categoria 2 (Hardware e Som).</td>
<td>Não se usa mais. Qualquer item que se adiciona apenas à categoria 4 aparece na categoria 2 (Hardware e Som).</td>
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
Quando não estiver conectado a um domínio, isso é chamado de Contas de &quot; Usuário e Segurança da &quot; Família.
</blockquote>
<br/></td>
<td>&quot;Contas de Usuário&quot;
<blockquote>
[!Note]<br />
Quando não estiver conectado a um domínio, isso é chamado de Contas de &quot; Usuário e Segurança da &quot; Família.
</blockquote>
<br/></td>
<td>&quot;Contas de Usuário&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Não se usa mais. Os itens registrados nessa categoria aparecem na categoria 5 (Sistema e Segurança).</td>
<td>&quot;Segurança&quot;</td>
<td>&quot;Central de Segurança&quot;
<blockquote>
[!Note]<br />
Disponível somente no Windows XP Service Pack 2 (SP2) ou posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>Não se usa mais. Os itens registrados nessa categoria aparecem na categoria 0 (Todos os Painel de Controle Itens).</td>
<td>&quot;Pc móvel&quot;
<blockquote>
[!Note]<br />
Essa categoria só é visível em PCs móveis.
</blockquote>
<br/></td>
<td>Não usado.</td>
</tr>
</tbody>
</table>



 

No Windows XP, as categorias **Adicionar**  ou Remover Programas e Contas de Usuário funcionam de forma um pouco diferente de outras categorias no Painel de Controle. Quando um ou mais itens são adicionados a uma dessas duas categorias, o link associado no Painel de Controle abre uma página de categoria. Os itens registrados aparecem na parte inferior da página sob o título "ou Escolha um ícone Painel de Controle". Quando nenhum item é registrado para uma dessas categorias, o link associado no Painel de Controle invoca diretamente o item Windows padrão para essa categoria. No Windows Vista e posterior, a categoria **Programas** e a categoria **Contas de** Usuário não têm essa propriedade.

A **categoria Central de** Segurança, disponível somente no Windows XP SP2, também é um pouco não padrão. Clicar nessa categoria abre a **página Central de** Segurança em uma nova janela. Os itens registrados **para a Central de** Segurança aparecem na parte inferior dessa página sob o título Gerenciar configurações de segurança **para:**. Clicar em um ícone abre o Painel de Controle item.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Painel de Controle itens](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando Painel de Controle itens](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Painel de Controle processamento de mensagens](message-processing.md)
</dt> <dt>

[Executando Painel de Controle itens](executing-control-panel-items.md)
</dt> <dt>

[Estendendo itens Painel de Controle sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Criando links de tarefa pesquisáveis para um Painel de Controle item](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o Painel de Controle no modo Cofre em Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




