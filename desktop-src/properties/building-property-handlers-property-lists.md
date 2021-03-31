---
description: Depois de avaliar sua estratégia de propriedade, você deve determinar quais propriedades mostrar na interface do usuário do Windows Explorer e onde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usando listas de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921343"
---
# <a name="using-property-lists"></a><span data-ttu-id="ae577-103">Usando listas de propriedades</span><span class="sxs-lookup"><span data-stu-id="ae577-103">Using Property Lists</span></span>

<span data-ttu-id="ae577-104">Depois de avaliar sua estratégia de propriedade, você deve determinar quais propriedades mostrar na interface do usuário do Windows Explorer e onde.</span><span class="sxs-lookup"><span data-stu-id="ae577-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="ae577-105">Há vários locais onde as propriedades são exibidas em uma maneira somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ae577-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="ae577-106">A edição de propriedade, por outro lado, é habilitada apenas na caixa de diálogo **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="ae577-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="ae577-107">Essa caixa de diálogo pode ser chamada por meio do link **Editar propriedades** no **painel de visualização** ou do menu de atalho de um item.</span><span class="sxs-lookup"><span data-stu-id="ae577-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="ae577-108">As listas de propriedades são cadeias de caracteres delimitadas por ponto e vírgula que têm o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="ae577-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="ae577-109">O único sinalizador disponível no momento é mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae577-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="ae577-110">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="ae577-110">Flag</span></span> | <span data-ttu-id="ae577-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae577-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="ae577-112">Não mostre a propriedade no painel de **Visualização** conforme instruído no valor da chave do registro **PreviewDetails** .</span><span class="sxs-lookup"><span data-stu-id="ae577-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="ae577-113">Consulte o exemplo que segue a próxima tabela se o valor da propriedade não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ae577-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="ae577-114">Depois de definir uma lista de propriedades, você pode armazenar essa cadeia de caracteres no registro por meio do sistema de [Associação de arquivo do Shell](../shell/fa-file-types.md) padrão sob a raiz de **\_ classes hKey \_ .**</span><span class="sxs-lookup"><span data-stu-id="ae577-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="ae577-115">A tabela a seguir resume os valores para as listas de propriedades que podem ser atribuídas na chave do registro para uma extensão de nome de arquivo específica.</span><span class="sxs-lookup"><span data-stu-id="ae577-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae577-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ae577-116">Value</span></span></th>
<th><span data-ttu-id="ae577-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae577-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae577-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae577-118">FullDetails</span></span></td>
<td><span data-ttu-id="ae577-119">As propriedades são exibidas na guia <strong>detalhes</strong> da caixa de diálogo <strong>Propriedades</strong> .</span><span class="sxs-lookup"><span data-stu-id="ae577-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="ae577-120">Esta é a lista completa de propriedades às quais o tipo de arquivo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="ae577-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae577-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="ae577-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="ae577-122">As propriedades são exibidas no <strong>painel de visualização</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae577-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae577-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="ae577-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="ae577-124">As propriedades são exibidas na área de título do <strong>painel de visualização</strong> ao lado da miniatura do item.</span><span class="sxs-lookup"><span data-stu-id="ae577-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="ae577-125">O número máximo de entradas é 3.</span><span class="sxs-lookup"><span data-stu-id="ae577-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="ae577-126">Se a lista de propriedades contiver mais do que o número máximo permitido, o restante das entradas será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ae577-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae577-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="ae577-127">TileInfo</span></span></td>
<td><span data-ttu-id="ae577-128">As propriedades são exibidas quando o modo de exibição de lista está no modo de exibição de <strong>blocos</strong> .</span><span class="sxs-lookup"><span data-stu-id="ae577-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="ae577-129">O número máximo de entradas é 3.</span><span class="sxs-lookup"><span data-stu-id="ae577-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="ae577-130">Se a lista de propriedades contiver mais do que o número máximo permitido, o restante das entradas será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ae577-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ae577-131">Esse valor estava presente no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae577-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae577-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="ae577-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="ae577-133">As propriedades são exibidas para um item quando o modo de exibição de lista está no modo de exibição de <strong>bloco estendido</strong> .</span><span class="sxs-lookup"><span data-stu-id="ae577-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae577-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="ae577-134">InfoTip</span></span></td>
<td><span data-ttu-id="ae577-135">As propriedades são exibidas em uma InfoTip quando um usuário passa o mouse sobre um item.</span><span class="sxs-lookup"><span data-stu-id="ae577-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ae577-136">Esse valor estava presente no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae577-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae577-137">QuickTip</span><span class="sxs-lookup"><span data-stu-id="ae577-137">QuickTip</span></span></td>
<td><span data-ttu-id="ae577-138">As propriedades são exibidas quando é difícil recuperar as propriedades diretamente de um item, como quando o item deve ser acessado por uma conexão de rede lenta.</span><span class="sxs-lookup"><span data-stu-id="ae577-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="ae577-139">É recomendável que as propriedades nomeadas aqui, como tipo ou tamanho, não exijam a abertura do fluxo de arquivos para determinar seu valor.</span><span class="sxs-lookup"><span data-stu-id="ae577-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ae577-140">Esse valor estava presente no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae577-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ae577-141">O exemplo a seguir define o valor de PreviewDetails para um tipo de arquivo. Recipe, usando um ProgID de **RecipeKey**.</span><span class="sxs-lookup"><span data-stu-id="ae577-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="ae577-142">Conforme explicado no tópico [Associação de arquivo do Shell](../shell/fa-file-types.md) , as associações de arquivo podem ser descritas para o mais específico para a forma mais geral.</span><span class="sxs-lookup"><span data-stu-id="ae577-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="ae577-143">A forma mais específica é a extensão de nome de arquivo único e a forma mais genérica é uma chave que se aplica a todos os arquivos e pastas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ae577-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="ae577-144">Entre esses dois extremos, você também pode definir um [ProgID](../shell/fa-progids.md) que agrupa um conjunto de extensões de nome de arquivo (por exemplo, os tipos. jpg e. jpeg agrupados como **jpegfile**).</span><span class="sxs-lookup"><span data-stu-id="ae577-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="ae577-145">Ao definir listas de propriedades, você deve defini-las para ProgIDs ou, em alguns casos, extensões de nome de arquivo específicas.</span><span class="sxs-lookup"><span data-stu-id="ae577-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="ae577-146">Evite depender de entradas amplas, como a chave **AllFileSystemObjects** .</span><span class="sxs-lookup"><span data-stu-id="ae577-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae577-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae577-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae577-148">Noções básicas sobre manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="ae577-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="ae577-149">Usando nomes de tipos</span><span class="sxs-lookup"><span data-stu-id="ae577-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="ae577-150">Inicializando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="ae577-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="ae577-151">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="ae577-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="ae577-152">Práticas recomendadas e perguntas frequentes do manipulador de propriedades</span><span class="sxs-lookup"><span data-stu-id="ae577-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
