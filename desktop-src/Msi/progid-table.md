---
description: A tabela ProgId contém informações para IDs de programa e IDs de programa independentes de versão que devem ser geradas como parte do anúncio do produto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabela ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922739"
---
# <a name="progid-table"></a><span data-ttu-id="c4b82-103">Tabela ProgId</span><span class="sxs-lookup"><span data-stu-id="c4b82-103">ProgId Table</span></span>

<span data-ttu-id="c4b82-104">A tabela ProgId contém informações para IDs de programa e IDs de programa independentes de versão que devem ser geradas como parte do anúncio do produto.</span><span class="sxs-lookup"><span data-stu-id="c4b82-104">The ProgId table contains information for program IDs and version independent program IDs that must be generated as a part of the product advertisement.</span></span>

<span data-ttu-id="c4b82-105">A tabela ProgId tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4b82-105">The ProgId table has the following columns.</span></span>



| <span data-ttu-id="c4b82-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="c4b82-106">Column</span></span>         | <span data-ttu-id="c4b82-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4b82-107">Type</span></span>                         | <span data-ttu-id="c4b82-108">Chave</span><span class="sxs-lookup"><span data-stu-id="c4b82-108">Key</span></span> | <span data-ttu-id="c4b82-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="c4b82-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="c4b82-110">ProgId</span><span class="sxs-lookup"><span data-stu-id="c4b82-110">ProgId</span></span>         | [<span data-ttu-id="c4b82-111">Text</span><span class="sxs-lookup"><span data-stu-id="c4b82-111">Text</span></span>](text.md)             | <span data-ttu-id="c4b82-112">S</span><span class="sxs-lookup"><span data-stu-id="c4b82-112">Y</span></span>   | <span data-ttu-id="c4b82-113">N</span><span class="sxs-lookup"><span data-stu-id="c4b82-113">N</span></span>        |
| <span data-ttu-id="c4b82-114">Pai do ProgId \_</span><span class="sxs-lookup"><span data-stu-id="c4b82-114">ProgId\_Parent</span></span> | [<span data-ttu-id="c4b82-115">Text</span><span class="sxs-lookup"><span data-stu-id="c4b82-115">Text</span></span>](text.md)             | <span data-ttu-id="c4b82-116">N</span><span class="sxs-lookup"><span data-stu-id="c4b82-116">N</span></span>   | <span data-ttu-id="c4b82-117">S</span><span class="sxs-lookup"><span data-stu-id="c4b82-117">Y</span></span>        |
| <span data-ttu-id="c4b82-118">Classe\_</span><span class="sxs-lookup"><span data-stu-id="c4b82-118">Class\_</span></span>        | [<span data-ttu-id="c4b82-119">GUID</span><span class="sxs-lookup"><span data-stu-id="c4b82-119">GUID</span></span>](guid.md)             | <span data-ttu-id="c4b82-120">N</span><span class="sxs-lookup"><span data-stu-id="c4b82-120">N</span></span>   | <span data-ttu-id="c4b82-121">S</span><span class="sxs-lookup"><span data-stu-id="c4b82-121">Y</span></span>        |
| <span data-ttu-id="c4b82-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4b82-122">Description</span></span>    | [<span data-ttu-id="c4b82-123">Text</span><span class="sxs-lookup"><span data-stu-id="c4b82-123">Text</span></span>](text.md)             | <span data-ttu-id="c4b82-124">N</span><span class="sxs-lookup"><span data-stu-id="c4b82-124">N</span></span>   | <span data-ttu-id="c4b82-125">S</span><span class="sxs-lookup"><span data-stu-id="c4b82-125">Y</span></span>        |
| <span data-ttu-id="c4b82-126">ícone\_</span><span class="sxs-lookup"><span data-stu-id="c4b82-126">Icon\_</span></span>         | [<span data-ttu-id="c4b82-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="c4b82-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="c4b82-128">N</span><span class="sxs-lookup"><span data-stu-id="c4b82-128">N</span></span>   | <span data-ttu-id="c4b82-129">S</span><span class="sxs-lookup"><span data-stu-id="c4b82-129">Y</span></span>        |
| <span data-ttu-id="c4b82-130">IconIndex</span><span class="sxs-lookup"><span data-stu-id="c4b82-130">IconIndex</span></span>      | [<span data-ttu-id="c4b82-131">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c4b82-131">Integer</span></span>](integer.md)       | <span data-ttu-id="c4b82-132">N</span><span class="sxs-lookup"><span data-stu-id="c4b82-132">N</span></span>   | <span data-ttu-id="c4b82-133">S</span><span class="sxs-lookup"><span data-stu-id="c4b82-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c4b82-134">Colunas</span><span class="sxs-lookup"><span data-stu-id="c4b82-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c4b82-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span><span class="sxs-lookup"><span data-stu-id="c4b82-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span></span>
</dt> <dd>

<span data-ttu-id="c4b82-136">A ID do programa ou a ID do programa independente da versão.</span><span class="sxs-lookup"><span data-stu-id="c4b82-136">The program ID or version independent program ID.</span></span> <span data-ttu-id="c4b82-137">Os ProgIds listados na tabela ProgId serão registrados se o CLSID listado na coluna classe \_ desta tabela estiver agendado para ser anunciado ou instalado.</span><span class="sxs-lookup"><span data-stu-id="c4b82-137">ProgIds listed in the ProgId table are registered if the CLSID listed in the Class\_column of this table is scheduled to be advertised or installed.</span></span> <span data-ttu-id="c4b82-138">Quando o ProgId é selecionado para registro, todos os ProgIds que se referem a essa linha por meio da \_ coluna pai ProgID também são selecionados para registro.</span><span class="sxs-lookup"><span data-stu-id="c4b82-138">When the ProgId is selected for registration, all ProgIds that refer to this row through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="c4b82-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>Pai do ProgId \_</span><span class="sxs-lookup"><span data-stu-id="c4b82-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="c4b82-140">Definido somente para IDs de programa independentes de versão.</span><span class="sxs-lookup"><span data-stu-id="c4b82-140">Defined only for version independent program IDs.</span></span> <span data-ttu-id="c4b82-141">Esse campo é uma chave estrangeira na coluna ProgId.</span><span class="sxs-lookup"><span data-stu-id="c4b82-141">This field is a foreign key into the ProgId column.</span></span> <span data-ttu-id="c4b82-142">Para definir uma ID de programa independente de versão, insira o ProgId correspondente na \_ coluna pai do ProgID.</span><span class="sxs-lookup"><span data-stu-id="c4b82-142">To define a version independent program ID, enter the corresponding ProgId into the ProgId\_Parent column.</span></span> <span data-ttu-id="c4b82-143">Quando o ProgId é selecionado para instalação, os ProgIds independentes de versão correspondentes associados por meio da \_ coluna pai do ProgID também são selecionados para registro.</span><span class="sxs-lookup"><span data-stu-id="c4b82-143">When the ProgId is selected for installation, the corresponding version-independent ProgIds associated through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="c4b82-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Classes\_</span><span class="sxs-lookup"><span data-stu-id="c4b82-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Class\_</span></span>
</dt> <dd>

<span data-ttu-id="c4b82-145">Uma chave estrangeira opcional na [tabela de classes](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4b82-145">An optional foreign key into the [Class table](class-table.md).</span></span> <span data-ttu-id="c4b82-146">Esta coluna deve ser nula para uma ProgId independente de versão.</span><span class="sxs-lookup"><span data-stu-id="c4b82-146">This column must be Null for a version independent ProgId.</span></span> <span data-ttu-id="c4b82-147">Se o valor de classe \_ de um ProgID for nulo, o ProgID será registrado quando aparecer na coluna ProgID de uma linha na tabela de [extensão](extension-table.md) e a extensão tiver pelo menos um verbo associado a ele na tabela de [verbos](verb-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4b82-147">If the Class\_value for a ProgId is null, the ProgId is registered when it appears in the ProgId column of a row in the [Extension table](extension-table.md) and the extension has at least one Verb associated with it in the [Verb table](verb-table.md).</span></span> <span data-ttu-id="c4b82-148">ProgIds selecionados para registro dessa maneira não instalam outros ProgIds que referenciam a ProgId atual por meio do \_ valor padrão de ProgID.</span><span class="sxs-lookup"><span data-stu-id="c4b82-148">ProgIds selected for registration in this manner do not install other ProgIds that reference the current ProgId through the ProgId\_Default value.</span></span>

</dd> <dt>

<span data-ttu-id="c4b82-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="c4b82-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="c4b82-150">Uma descrição opcional localizada da ID do programa associada.</span><span class="sxs-lookup"><span data-stu-id="c4b82-150">An optional localized description of the associated program ID.</span></span>

</dd> <dt>

<span data-ttu-id="c4b82-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Cone\_</span><span class="sxs-lookup"><span data-stu-id="c4b82-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="c4b82-152">Uma chave estrangeira opcional na [tabela de ícones](icon-table.md) que especifica o arquivo de ícone associado a este ProgID.</span><span class="sxs-lookup"><span data-stu-id="c4b82-152">An optional foreign key into the [Icon table](icon-table.md) that specifies the icon file associated with this ProgId.</span></span> <span data-ttu-id="c4b82-153">Isso é escrito sob a chave DefaultIcon associada a este ProgId.</span><span class="sxs-lookup"><span data-stu-id="c4b82-153">This is written under the DefaultIcon key associated with this ProgId.</span></span> <span data-ttu-id="c4b82-154">Esta coluna deve ser nula para uma ProgId independente de versão.</span><span class="sxs-lookup"><span data-stu-id="c4b82-154">This column must be Null for a version independent ProgId.</span></span>

</dd> <dt>

<span data-ttu-id="c4b82-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="c4b82-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="c4b82-156">O índice de ícone no arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="c4b82-156">The Icon index into the icon file.</span></span> <span data-ttu-id="c4b82-157">Esta coluna deve ser nula para uma ProgId independente de versão.</span><span class="sxs-lookup"><span data-stu-id="c4b82-157">This column must be Null for a version independent ProgId.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4b82-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4b82-158">Remarks</span></span>

<span data-ttu-id="c4b82-159">As ações [RegisterProgIdInfo](registerprogidinfo-action.md) e [UnregisterProgIdInfo](unregisterprogidinfo-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c4b82-159">The [RegisterProgIdInfo](registerprogidinfo-action.md) and [UnregisterProgIdInfo](unregisterprogidinfo-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="c4b82-160">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4b82-160">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c4b82-161">Validação</span><span class="sxs-lookup"><span data-stu-id="c4b82-161">Validation</span></span>

<dl>

[<span data-ttu-id="c4b82-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="c4b82-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c4b82-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="c4b82-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c4b82-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="c4b82-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c4b82-165">ICE36</span><span class="sxs-lookup"><span data-stu-id="c4b82-165">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="c4b82-166">ICE89</span><span class="sxs-lookup"><span data-stu-id="c4b82-166">ICE89</span></span>](ice89.md)  
</dl>

 

 



