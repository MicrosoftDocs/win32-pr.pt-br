---
description: Exibindo informações de topologia
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Exibindo informações de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797553"
---
# <a name="viewing-topology-information"></a><span data-ttu-id="ef187-103">Exibindo informações de topologia</span><span class="sxs-lookup"><span data-stu-id="ef187-103">Viewing Topology Information</span></span>

<span data-ttu-id="ef187-104">No TopoEdit, cada item de topologia, como nós, entradas de nó e saídas de nó, tem um repositório de atributos associado que gerencia o comportamento do nó.</span><span class="sxs-lookup"><span data-stu-id="ef187-104">In TopoEdit, each topology item, such as nodes, node inputs, and node outputs, has an associated attribute store that manages the behavior of the node.</span></span> <span data-ttu-id="ef187-105">Para ver os atributos, selecione o item e o **painel atributos** exibe as informações.</span><span class="sxs-lookup"><span data-stu-id="ef187-105">To see the attributes, select the item, and the **Attributes Pane** displays the information.</span></span> <span data-ttu-id="ef187-106">Para topologias que são carregadas de um arquivo XML, alguns dos nós podem não exibir todo o repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="ef187-106">For topologies that are loaded from an XML file, some of the nodes may not display the entire attribute store.</span></span> <span data-ttu-id="ef187-107">Para ver todo o repositório de atributos, resolva a topologia.</span><span class="sxs-lookup"><span data-stu-id="ef187-107">To see the entire attribute store, resolve the topology.</span></span> <span data-ttu-id="ef187-108">Para obter mais informações, consulte [resolvendo uma topologia com TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="ef187-108">For more information, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="ef187-109">A tabela a seguir mostra o item de topologia e os atributos que o painel exibe.</span><span class="sxs-lookup"><span data-stu-id="ef187-109">The following table shows the topology item and the attributes that the pane displays.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef187-110">Item de topologia</span><span class="sxs-lookup"><span data-stu-id="ef187-110">Topology item</span></span></th>
<th><span data-ttu-id="ef187-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef187-111">Attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef187-112">Nós de topologia</span><span class="sxs-lookup"><span data-stu-id="ef187-112">Topology nodes</span></span></td>
<td><ul>
<li><span data-ttu-id="ef187-113"><a href="topology-node-attributes.md">Atributos de nó de topologia</a> para todos os nós.</span><span class="sxs-lookup"><span data-stu-id="ef187-113"><a href="topology-node-attributes.md">Topology Node Attributes</a> for all nodes.</span></span><br/></li>
<li><span data-ttu-id="ef187-114"><a href="presentation-descriptor-attributes.md">Atributos de descritor de apresentação</a> somente para nós de origem.</span><span class="sxs-lookup"><span data-stu-id="ef187-114"><a href="presentation-descriptor-attributes.md">Presentation Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="ef187-115">Informações de autoridade de confiança de entrada e saída para nós de transformação e saída.</span><span class="sxs-lookup"><span data-stu-id="ef187-115">Input and output trust authority information for transform and output nodes.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef187-116">Entrada de nó</span><span class="sxs-lookup"><span data-stu-id="ef187-116">Node input</span></span></td>
<td><ul>
<li><span data-ttu-id="ef187-117"><a href="media-type-attributes.md">Atributos de tipo de mídia</a> para todos os nós.</span><span class="sxs-lookup"><span data-stu-id="ef187-117"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef187-118">Saída de nó</span><span class="sxs-lookup"><span data-stu-id="ef187-118">Node output</span></span></td>
<td><ul>
<li><span data-ttu-id="ef187-119"><a href="stream-descriptor-attributes.md">Atributos de descritor de fluxo</a> somente para nós de origem.</span><span class="sxs-lookup"><span data-stu-id="ef187-119"><a href="stream-descriptor-attributes.md">Stream Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="ef187-120"><a href="media-type-attributes.md">Atributos de tipo de mídia</a> para todos os nós.</span><span class="sxs-lookup"><span data-stu-id="ef187-120"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span><br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ef187-121">Os valores de atributo, exceto para referências de ponteiro e valores de matriz, podem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="ef187-121">The attribute values, except for pointer references and array values, can be changed.</span></span> <span data-ttu-id="ef187-122">Para alterar um valor de atributo, digite o novo valor ao lado do atributo e clique em **salvar** no **painel atributos**.</span><span class="sxs-lookup"><span data-stu-id="ef187-122">To change an attribute value, type in the new value next to the attribute and click **Save** on the **Attributes Pane**.</span></span> <span data-ttu-id="ef187-123">O novo valor é atualizado no repositório de atributos e aplicado à topologia somente depois que ele é resolvido.</span><span class="sxs-lookup"><span data-stu-id="ef187-123">The new value is updated in the attribute store and applied to the topology only after it is resolved.</span></span>

## <a name="to-add-a-new-attribute-for-a-node"></a><span data-ttu-id="ef187-124">Para adicionar um novo atributo para um nó</span><span class="sxs-lookup"><span data-stu-id="ef187-124">To add a new attribute for a node</span></span>

1.  <span data-ttu-id="ef187-125">Selecione o nó clicando nele no **painel topologia**.</span><span class="sxs-lookup"><span data-stu-id="ef187-125">Select the node by clicking it on the **Topology Pane**.</span></span>

    <span data-ttu-id="ef187-126">Os atributos definidos no nó são mostrados no **painel atributos**.</span><span class="sxs-lookup"><span data-stu-id="ef187-126">The attributes that are set on the node are shown on the **Attributes Pane**.</span></span>

2.  <span data-ttu-id="ef187-127">No **painel atributos**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ef187-127">On the **Attributes Pane**, click **Add**.</span></span>

    <span data-ttu-id="ef187-128">Isso abre a caixa de diálogo **Adicionar atributo** .</span><span class="sxs-lookup"><span data-stu-id="ef187-128">This opens the **Add Attribute** dialog box.</span></span>

3.  <span data-ttu-id="ef187-129">Na primeira lista suspensa, escolha a categoria de atributo.</span><span class="sxs-lookup"><span data-stu-id="ef187-129">From the first drop-down list, choose the Attribute category.</span></span>

    <span data-ttu-id="ef187-130">As categorias dependem do nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="ef187-130">The categories depend on the topology node.</span></span> <span data-ttu-id="ef187-131">Por exemplo, para o nó de origem, a lista suspensa mostra **atributos de descritor de apresentação** e atributos de **nó** como as categorias disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ef187-131">For example, for the source node, the drop-down list shows **Presentation Descriptor Attributes** and **Node Attributes** as the available categories.</span></span>

4.  <span data-ttu-id="ef187-132">Na segunda lista suspensa, escolha o atributo que você deseja definir no nó.</span><span class="sxs-lookup"><span data-stu-id="ef187-132">From the second drop-down list, choose the attribute that you want to set on the node.</span></span>

5.  <span data-ttu-id="ef187-133">Na caixa de edição, adicione o valor para o atributo.</span><span class="sxs-lookup"><span data-stu-id="ef187-133">In the edit box, add the value for the attribute.</span></span>

6.  <span data-ttu-id="ef187-134">Clique em **Adicionar** para adicionar o atributo e retornar à janela principal, ou clique em **Cancelar** para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="ef187-134">Click **Add** to add the attribute and return to the main window, or click **Cancel** to cancel the operation.</span></span>

7.  <span data-ttu-id="ef187-135">No menu **topologia** , clique em **resolver topologia** para definir o novo atributo para a topologia.</span><span class="sxs-lookup"><span data-stu-id="ef187-135">From the **Topology** menu, click **Resolve Topology** to set the new attribute to the topology.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef187-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef187-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef187-137">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="ef187-137">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




