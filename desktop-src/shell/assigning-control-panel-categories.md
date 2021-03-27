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
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="7971d-105">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7971d-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="7971d-106">A partir do Windows XP, o painel de controle oferece suporte à categorização de itens do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7971d-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="7971d-107">Os itens são registrados para aparecerem em uma ou mais categorias.</span><span class="sxs-lookup"><span data-stu-id="7971d-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="7971d-108">Não é possível criar novas categorias.</span><span class="sxs-lookup"><span data-stu-id="7971d-108">New categories cannot be created.</span></span>

<span data-ttu-id="7971d-109">Para registrar um item do painel de controle em uma ou mais categorias, adicione valores conforme explicado na seção registro do [item do painel de controle executável](registering-control-panel-items.md) ou [registro do item do painel de controle da dll](registering-control-panel-items.md) de registro de [itens](registering-control-panel-items.md)do painel de controle, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="7971d-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7971d-110">ID da categoria</span><span class="sxs-lookup"><span data-stu-id="7971d-110">Category ID</span></span></th>
<th><span data-ttu-id="7971d-111">Nome da categoria (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="7971d-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="7971d-112">Nome da categoria (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="7971d-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="7971d-113">Nome da categoria (Windows XP)</span><span class="sxs-lookup"><span data-stu-id="7971d-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7971d-114">0</span><span class="sxs-lookup"><span data-stu-id="7971d-114">0</span></span></td>
<td><span data-ttu-id="7971d-115">&quot;Todos os itens do painel de controle&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="7971d-116">&quot;Opções adicionais&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7971d-117">Qualquer item do painel de controle que não especifique uma ID de categoria aparece nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="7971d-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7971d-118">&quot;Outras opções do painel de controle&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7971d-119">Qualquer item do painel de controle que não especifique uma ID de categoria aparece nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="7971d-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7971d-120">1</span><span class="sxs-lookup"><span data-stu-id="7971d-120">1</span></span></td>
<td><span data-ttu-id="7971d-121">&quot;Aparência e Personalização&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="7971d-122">&quot;Aparência e Personalização&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="7971d-123">&quot;Aparência e temas&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7971d-124">2</span><span class="sxs-lookup"><span data-stu-id="7971d-124">2</span></span></td>
<td><span data-ttu-id="7971d-125">&quot;Hardware e som&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="7971d-126">&quot;Hardware e som&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="7971d-127">&quot;Impressoras e outros tipos de hardware&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7971d-128">3</span><span class="sxs-lookup"><span data-stu-id="7971d-128">3</span></span></td>
<td><span data-ttu-id="7971d-129">&quot;Rede e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="7971d-130">&quot;Rede e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="7971d-131">&quot;Conexões de rede e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7971d-132">4</span><span class="sxs-lookup"><span data-stu-id="7971d-132">4</span></span></td>
<td><span data-ttu-id="7971d-133">Não se usa mais.</span><span class="sxs-lookup"><span data-stu-id="7971d-133">No longer used.</span></span> <span data-ttu-id="7971d-134">Qualquer item que se adiciona somente à categoria 4 aparece na categoria 2 (hardware e som).</span><span class="sxs-lookup"><span data-stu-id="7971d-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="7971d-135">Não se usa mais.</span><span class="sxs-lookup"><span data-stu-id="7971d-135">No longer used.</span></span> <span data-ttu-id="7971d-136">Qualquer item que se adiciona somente à categoria 4 aparece na categoria 2 (hardware e som).</span><span class="sxs-lookup"><span data-stu-id="7971d-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="7971d-137">&quot;Sons, fala e dispositivos de áudio&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7971d-138">5</span><span class="sxs-lookup"><span data-stu-id="7971d-138">5</span></span></td>
<td><span data-ttu-id="7971d-139">&quot;Sistema e segurança&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="7971d-140">&quot;Sistema e manutenção&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="7971d-141">&quot;Desempenho e manutenção&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7971d-142">6</span><span class="sxs-lookup"><span data-stu-id="7971d-142">6</span></span></td>
<td><span data-ttu-id="7971d-143">&quot;Relógio, idioma e região&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="7971d-144">&quot;Relógio, idioma e região&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="7971d-145">&quot;Opções de data, hora, idioma e regionais&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7971d-146">7</span><span class="sxs-lookup"><span data-stu-id="7971d-146">7</span></span></td>
<td><span data-ttu-id="7971d-147">&quot;Facilidade de Acesso&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="7971d-148">&quot;Facilidade de Acesso&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="7971d-149">&quot;Opções de acessibilidade&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7971d-150">8</span><span class="sxs-lookup"><span data-stu-id="7971d-150">8</span></span></td>
<td><span data-ttu-id="7971d-151">&quot;Programas&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="7971d-152">&quot;Programas&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="7971d-153">&quot;Adicionar ou remover programas&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7971d-154">9</span><span class="sxs-lookup"><span data-stu-id="7971d-154">9</span></span></td>
<td><span data-ttu-id="7971d-155">&quot;Contas de Usuário&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7971d-156">Quando não conectado a um domínio, isso é chamado de &quot; contas de usuário e segurança de família &quot; .</span><span class="sxs-lookup"><span data-stu-id="7971d-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7971d-157">&quot;Contas de Usuário&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7971d-158">Quando não conectado a um domínio, isso é chamado de &quot; contas de usuário e segurança de família &quot; .</span><span class="sxs-lookup"><span data-stu-id="7971d-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7971d-159">&quot;Contas de Usuário&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7971d-160">10</span><span class="sxs-lookup"><span data-stu-id="7971d-160">10</span></span></td>
<td><span data-ttu-id="7971d-161">Não se usa mais.</span><span class="sxs-lookup"><span data-stu-id="7971d-161">No longer used.</span></span> <span data-ttu-id="7971d-162">Os itens registrados nessa categoria aparecem na categoria 5 (sistema e segurança).</span><span class="sxs-lookup"><span data-stu-id="7971d-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="7971d-163">&quot;Segurança&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="7971d-164">&quot;Central de Segurança&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7971d-165">Disponível apenas no Windows XP Service Pack 2 (SP2) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7971d-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7971d-166">11</span><span class="sxs-lookup"><span data-stu-id="7971d-166">11</span></span></td>
<td><span data-ttu-id="7971d-167">Não se usa mais.</span><span class="sxs-lookup"><span data-stu-id="7971d-167">No longer used.</span></span> <span data-ttu-id="7971d-168">Os itens registrados nessa categoria aparecem na categoria 0 (todos os itens do painel de controle).</span><span class="sxs-lookup"><span data-stu-id="7971d-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="7971d-169">&quot;PC móvel&quot;</span><span class="sxs-lookup"><span data-stu-id="7971d-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7971d-170">Essa categoria só é visível em PCs móveis.</span><span class="sxs-lookup"><span data-stu-id="7971d-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7971d-171">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7971d-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7971d-172">No Windows XP, as categorias **adicionam ou removem programas** e **contas de usuário** funcionam de maneira um pouco diferente de outras categorias no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7971d-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="7971d-173">Quando um ou mais itens são adicionados a uma dessas duas categorias, o link associado no painel de controle abre uma página de categoria.</span><span class="sxs-lookup"><span data-stu-id="7971d-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="7971d-174">Os itens registrados aparecem na parte inferior da página sob o título "ou selecionam um ícone do painel de controle".</span><span class="sxs-lookup"><span data-stu-id="7971d-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="7971d-175">Quando nenhum item é registrado para uma dessas categorias, o link associado no painel de controle chama diretamente o item padrão do Windows para essa categoria.</span><span class="sxs-lookup"><span data-stu-id="7971d-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="7971d-176">No Windows Vista e posterior, a categoria **programas** e a categoria **contas de usuário** não têm essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7971d-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="7971d-177">A categoria da **central de segurança** , disponível apenas no Windows XP SP2, também é um pouco não padrão.</span><span class="sxs-lookup"><span data-stu-id="7971d-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="7971d-178">Clicar nessa categoria abre a página **central de segurança** em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="7971d-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="7971d-179">Os itens registrados para a **central de segurança** aparecem na parte inferior dessa página, sob o título **gerenciar configurações de segurança para:**.</span><span class="sxs-lookup"><span data-stu-id="7971d-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="7971d-180">Clicar em um ícone abre o item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7971d-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7971d-181">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7971d-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7971d-182">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7971d-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="7971d-183">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="7971d-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="7971d-184">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7971d-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="7971d-185">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="7971d-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="7971d-186">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7971d-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="7971d-187">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7971d-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="7971d-188">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="7971d-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="7971d-189">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7971d-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="7971d-190">Acessando o painel de controle no modo de segurança no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7971d-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




