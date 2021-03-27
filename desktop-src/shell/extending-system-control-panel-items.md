---
description: Alguns dos itens do sistema encontrados no painel de controle são extensíveis. Para instalar uma extensão do painel de controle, registre a extensão do Shell da seguinte maneira, em que nome é o nome predefinido do item do sistema (consulte a tabela abaixo).
title: Estendendo itens do painel de controle do sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988780"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="08e5b-104">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="08e5b-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="08e5b-105">Alguns dos itens do sistema encontrados no painel de controle são extensíveis.</span><span class="sxs-lookup"><span data-stu-id="08e5b-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="08e5b-106">Para instalar uma extensão do painel de controle, registre a extensão do Shell da seguinte maneira, em que *nome* é o nome predefinido do item do sistema (consulte a tabela abaixo).</span><span class="sxs-lookup"><span data-stu-id="08e5b-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="08e5b-107">Isso é semelhante à maneira como você registraria uma extensão para um objeto de shell predefinido.</span><span class="sxs-lookup"><span data-stu-id="08e5b-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="08e5b-108">Como as únicas extensões do Shell suportadas pelos itens do painel de controle são folhas de propriedades, o registro deve estar na subchave **shellex** \\ **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="08e5b-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08e5b-109">Item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-109">Control Panel item</span></span></th>
<th><span data-ttu-id="08e5b-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="08e5b-110"><em>name</em></span></span></th>
<th><span data-ttu-id="08e5b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="08e5b-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08e5b-112">Monitor</span><span class="sxs-lookup"><span data-stu-id="08e5b-112">Display</span></span></td>
<td><span data-ttu-id="08e5b-113">Escritório</span><span class="sxs-lookup"><span data-stu-id="08e5b-113">Desk</span></span></td>
<td><span data-ttu-id="08e5b-114">Também dá suporte à substituição da página <strong>da área de trabalho</strong> .</span><span class="sxs-lookup"><span data-stu-id="08e5b-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="08e5b-115">Não há mais suporte para isso no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08e5b-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e5b-116">Configurações de exibição avançadas</span><span class="sxs-lookup"><span data-stu-id="08e5b-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="08e5b-117">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="08e5b-117">Device</span></span></td>
<td><span data-ttu-id="08e5b-118">Propriedades avançadas específicas de não-difíceis.</span><span class="sxs-lookup"><span data-stu-id="08e5b-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="08e5b-119">Não há mais suporte para isso no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08e5b-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08e5b-120">Configurações de exibição avançadas</span><span class="sxs-lookup"><span data-stu-id="08e5b-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="08e5b-121">Monitor</span><span class="sxs-lookup"><span data-stu-id="08e5b-121">Display</span></span></td>
<td><span data-ttu-id="08e5b-122">Propriedades avançadas específicas de hardware.</span><span class="sxs-lookup"><span data-stu-id="08e5b-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="08e5b-123">Não há mais suporte para isso no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08e5b-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e5b-124">Opções da Internet</span><span class="sxs-lookup"><span data-stu-id="08e5b-124">Internet Options</span></span></td>
<td><span data-ttu-id="08e5b-125">Internet</span><span class="sxs-lookup"><span data-stu-id="08e5b-125">Internet</span></span></td>
<td><span data-ttu-id="08e5b-126">O número máximo de páginas de extensão é 18.</span><span class="sxs-lookup"><span data-stu-id="08e5b-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08e5b-127">Teclado</span><span class="sxs-lookup"><span data-stu-id="08e5b-127">Keyboard</span></span></td>
<td><span data-ttu-id="08e5b-128">Teclado</span><span class="sxs-lookup"><span data-stu-id="08e5b-128">Keyboard</span></span></td>
<td><span data-ttu-id="08e5b-129">O número máximo de páginas de extensão é 30.</span><span class="sxs-lookup"><span data-stu-id="08e5b-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e5b-130">Mouse</span><span class="sxs-lookup"><span data-stu-id="08e5b-130">Mouse</span></span></td>
<td><span data-ttu-id="08e5b-131">Mouse</span><span class="sxs-lookup"><span data-stu-id="08e5b-131">Mouse</span></span></td>
<td><span data-ttu-id="08e5b-132">Também dá suporte à substituição de páginas padrão.</span><span class="sxs-lookup"><span data-stu-id="08e5b-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="08e5b-133">O número máximo de páginas de extensão é 8.</span><span class="sxs-lookup"><span data-stu-id="08e5b-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08e5b-134">Opções de Energia</span><span class="sxs-lookup"><span data-stu-id="08e5b-134">Power Options</span></span></td>
<td><span data-ttu-id="08e5b-135">Energia</span><span class="sxs-lookup"><span data-stu-id="08e5b-135">Power</span></span></td>
<td><span data-ttu-id="08e5b-136">O número máximo de páginas, incluindo páginas padrão, é 18.</span><span class="sxs-lookup"><span data-stu-id="08e5b-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e5b-137">Sistema</span><span class="sxs-lookup"><span data-stu-id="08e5b-137">System</span></span></td>
<td><span data-ttu-id="08e5b-138">Sistema</span><span class="sxs-lookup"><span data-stu-id="08e5b-138">System</span></span></td>
<td><span data-ttu-id="08e5b-139">O número máximo de páginas de extensão é 8.</span><span class="sxs-lookup"><span data-stu-id="08e5b-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="08e5b-140">Não há mais suporte para isso no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08e5b-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="08e5b-141">O item **Adicionar ou remover programas** no painel de controle do Windows XP não é uma folha de propriedades e, portanto, não pode ser estendido pelos métodos discutidos aqui.</span><span class="sxs-lookup"><span data-stu-id="08e5b-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="08e5b-142">Em vez disso, seu conteúdo é obtido de Publicadores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="08e5b-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="08e5b-143">Para obter mais informações sobre como adicionar conteúdo para **Adicionar ou remover programas**, consulte [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span><span class="sxs-lookup"><span data-stu-id="08e5b-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e5b-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08e5b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e5b-145">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="08e5b-146">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="08e5b-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="08e5b-147">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="08e5b-148">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="08e5b-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="08e5b-149">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="08e5b-150">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="08e5b-151">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="08e5b-152">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="08e5b-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="08e5b-153">Acessando o painel de controle no modo de segurança no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08e5b-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




