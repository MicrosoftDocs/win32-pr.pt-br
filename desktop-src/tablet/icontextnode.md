---
description: Representa um nó em uma árvore de objetos que são criados como parte da análise de tinta.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interface IContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010523"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="c3657-103">Interface IContextNode</span><span class="sxs-lookup"><span data-stu-id="c3657-103">IContextNode interface</span></span>

<span data-ttu-id="c3657-104">Representa um nó em uma árvore de objetos que são criados como parte da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="c3657-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="c3657-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c3657-105">Members</span></span>

<span data-ttu-id="c3657-106">A interface **IContextNode** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c3657-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c3657-107">**IContextNode** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c3657-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="c3657-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3657-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c3657-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3657-109">Methods</span></span>

<span data-ttu-id="c3657-110">A interface **IContextNode** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c3657-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="c3657-111">Método</span><span class="sxs-lookup"><span data-stu-id="c3657-111">Method</span></span>                                                                                  | <span data-ttu-id="c3657-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3657-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3657-113">**AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="c3657-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="c3657-114">Adiciona um novo [**IContextLink**](icontextlink.md) à coleção de links de contexto do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="c3657-115">**AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c3657-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="c3657-116">Adiciona uma parte dos dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3657-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="c3657-117">**Veja**</span><span class="sxs-lookup"><span data-stu-id="c3657-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="c3657-118">Modifica o tipo de confirmação, que controla o que o objeto [**IInkAnalyzer**](iinkanalyzer.md) pode alterar sobre o **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="c3657-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="c3657-119">**ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c3657-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="c3657-120">Determina se o objeto **IContextNode** contém dados armazenados no identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="c3657-121">**CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="c3657-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="c3657-122">Cria um objeto **IContextNode** filho que contém apenas informações sobre tipo, identificador e local.</span><span class="sxs-lookup"><span data-stu-id="c3657-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="c3657-123">**CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="c3657-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="c3657-124">Cria um novo objeto filho **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="c3657-125">**DeleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="c3657-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="c3657-126">Exclui um objeto [**IContextLink**](icontextlink.md) da coleção de links do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="c3657-127">**DeleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="c3657-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="c3657-128">Remove um **IContextNode** filho.</span><span class="sxs-lookup"><span data-stu-id="c3657-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c3657-129">**GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="c3657-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="c3657-130">Recupera uma coleção de objetos [**IContextLink**](icontextlink.md) que representa relações com outros objetos **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="c3657-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="c3657-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="c3657-132">Recupera o identificador para o objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="c3657-133">**GetLocation**</span><span class="sxs-lookup"><span data-stu-id="c3657-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="c3657-134">Recupera a posição e o tamanho do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="c3657-135">**GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="c3657-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="c3657-136">Recupera o nó pai desse **IContextNode** na árvore de nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="c3657-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="c3657-137">**GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="c3657-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="c3657-138">Recupera o valor que indica se um objeto **IContextNode** está parcialmente populado ou totalmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="c3657-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="c3657-139">**GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c3657-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="c3657-140">Recupera dados específicos do aplicativo ou outros dados de propriedade de acordo com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="c3657-141">**GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="c3657-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="c3657-142">Recupera os identificadores para os quais há dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3657-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c3657-143">**GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="c3657-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="c3657-144">Recupera o número de traços associados ao objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="c3657-145">**Getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="c3657-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="c3657-146">Recupera o identificador de traço para o traço referenciado por um valor de índice dentro do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="c3657-147">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="c3657-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="c3657-148">Recupera uma matriz de identificadores para os traços dentro do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="c3657-149">**GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="c3657-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="c3657-150">Recupera uma matriz que contém os dados de Propriedade do pacote para o traço especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="c3657-151">**GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="c3657-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="c3657-152">Recupera uma matriz que contém os identificadores de propriedade de pacote para o traço especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="c3657-153">**GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="c3657-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="c3657-154">Recupera os nós filho diretos do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="c3657-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="c3657-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="c3657-156">Recupera o tipo do objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="c3657-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="c3657-157">**GetTypeName**</span><span class="sxs-lookup"><span data-stu-id="c3657-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="c3657-158">Recupera um nome de tipo legível por humanos deste **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="c3657-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="c3657-159">**IsDeleted**</span><span class="sxs-lookup"><span data-stu-id="c3657-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="c3657-160">Recupera um valor que indica se o objeto **IContextNode** é confirmado.</span><span class="sxs-lookup"><span data-stu-id="c3657-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="c3657-161">[**IInkAnalyzer**](iinkanalyzer.md) não pode alterar o tipo de nó e os traços associados para objetos **IContextNode** confirmados.</span><span class="sxs-lookup"><span data-stu-id="c3657-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="c3657-162">**LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="c3657-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="c3657-163">Recria os dados de propriedade interna e específica do aplicativo para uma matriz de bytes que foi criada anteriormente com [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="c3657-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="c3657-164">**MoveSubNodeToPosition**</span><span class="sxs-lookup"><span data-stu-id="c3657-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="c3657-165">Reordena um objeto **IContextNode** filho especificado para o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="c3657-166">**RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="c3657-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="c3657-167">Remove uma parte dos dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3657-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="c3657-168">**Reassociar**</span><span class="sxs-lookup"><span data-stu-id="c3657-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="c3657-169">Move este objeto **IContextNode** da coleção de subnós do seu nó de contexto pai para a coleção de subnós do nó de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="c3657-170">**ReparentStrokeByIdToNode**</span><span class="sxs-lookup"><span data-stu-id="c3657-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="c3657-171">Move os dados de traço deste **IContextNode** para o **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="c3657-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="c3657-172">**SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="c3657-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="c3657-173">Recupera uma matriz de bytes que contém os dados de propriedade internos e específicos do aplicativo para este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="c3657-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="c3657-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="c3657-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="c3657-175">Atualiza a posição e o tamanho deste **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="c3657-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="c3657-176">**SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="c3657-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="c3657-177">Modifica o valor que indica se este **IContextNode** está parcialmente ou totalmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="c3657-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="c3657-178">**Os traços**</span><span class="sxs-lookup"><span data-stu-id="c3657-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="c3657-179">Associa os traços especificados a este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="c3657-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c3657-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3657-180">Remarks</span></span>

<span data-ttu-id="c3657-181">Os tipos de nós são descritos nas constantes de [tipos de nó de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="c3657-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="c3657-182">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3657-182">Examples</span></span>

<span data-ttu-id="c3657-183">O exemplo a seguir mostra um método que examina um **IContextNode**; o método faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3657-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="c3657-184">Obtém o tipo do nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="c3657-184">Gets the context node's type.</span></span> <span data-ttu-id="c3657-185">Se o nó de contexto for uma tinta não classificada, uma dica de análise ou um nó de reconhecedor personalizado, ele chamará um método auxiliar para examinar propriedades específicas do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="c3657-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="c3657-186">Se o nó tiver subnós, ele examinará cada subnó chamando a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="c3657-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="c3657-187">Se o nó for um nó folha de tinta, ele examinará os dados de traço do nó chamando um método auxiliar.</span><span class="sxs-lookup"><span data-stu-id="c3657-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="c3657-188">A API a InkAnalysis permite que você crie um nó de linha que contém palavras de tinta e palavras de texto.</span><span class="sxs-lookup"><span data-stu-id="c3657-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="c3657-189">No entanto, o analisador irá ignorar esses nós mistos e os tratará como nós estrangeiros.</span><span class="sxs-lookup"><span data-stu-id="c3657-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="c3657-190">Isso terá impacto sobre a precisão da análise da detecção de anotações de tinta quando o usuário final grava ou circunda esse nó misto.</span><span class="sxs-lookup"><span data-stu-id="c3657-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c3657-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3657-191">Requirements</span></span>



| <span data-ttu-id="c3657-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3657-192">Requirement</span></span> | <span data-ttu-id="c3657-193">Valor</span><span class="sxs-lookup"><span data-stu-id="c3657-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3657-194">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3657-194">Minimum supported client</span></span><br/> | <span data-ttu-id="c3657-195">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c3657-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3657-196">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3657-196">Minimum supported server</span></span><br/> | <span data-ttu-id="c3657-197">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c3657-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c3657-198">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3657-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3657-199"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c3657-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c3657-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c3657-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3657-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3657-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c3657-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3657-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3657-203">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="c3657-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="c3657-204">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="c3657-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="c3657-205">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c3657-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c3657-206">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="c3657-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

