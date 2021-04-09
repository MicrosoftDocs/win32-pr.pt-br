---
description: Os componentes qualificados são um método de indireção e podem ser usados para agrupar componentes com funcionalidade paralela em categorias.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Usando componentes qualificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090475"
---
# <a name="using-qualified-components"></a><span data-ttu-id="72f0c-103">Usando componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="72f0c-103">Using Qualified Components</span></span>

<span data-ttu-id="72f0c-104">Os componentes qualificados são um método de indireção e podem ser usados para agrupar componentes com funcionalidade paralela em categorias.</span><span class="sxs-lookup"><span data-stu-id="72f0c-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="72f0c-105">Para retornar o caminho completo e instalar um [componente qualificado](qualified-components.md), chame [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span><span class="sxs-lookup"><span data-stu-id="72f0c-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="72f0c-106">Para enumerar todos os qualificadores de componente qualificados e cadeias de caracteres descritivas, chame [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="72f0c-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="72f0c-107">**Para agrupar componentes em uma categoria de componente qualificado**</span><span class="sxs-lookup"><span data-stu-id="72f0c-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="72f0c-108">Deve haver um registro na tabela de [componentes](component-table.md) para cada componente incluído na nova categoria de componentes qualificados.</span><span class="sxs-lookup"><span data-stu-id="72f0c-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="72f0c-109">Crie os campos na tabela de componentes da mesma forma que para componentes comuns.</span><span class="sxs-lookup"><span data-stu-id="72f0c-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="72f0c-110">Observe que cada componente qualificado deve ter um GUID de ID de componente exclusivo inserido na coluna ComponentID da tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="72f0c-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="72f0c-111">Gere uma cadeia de texto de qualificador para cada componente qualificado.</span><span class="sxs-lookup"><span data-stu-id="72f0c-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="72f0c-112">O qualificador deve ser uma cadeia de caracteres de texto exclusiva que pode ser facilmente gerada ao pesquisar um componente qualificado.</span><span class="sxs-lookup"><span data-stu-id="72f0c-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="72f0c-113">Por exemplo, se os componentes na categoria estiverem sendo qualificados por idioma, o LCID (identificador de localidade numérica) será uma cadeia de caracteres de qualificador razoável.</span><span class="sxs-lookup"><span data-stu-id="72f0c-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="72f0c-114">Adicione um registro na [tabela PublishComponent](publishcomponent-table.md) para cada componente qualificado.</span><span class="sxs-lookup"><span data-stu-id="72f0c-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="72f0c-115">Insira os identificadores de componente qualificados da coluna componente da tabela componente na \_ coluna componente da tabela PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="72f0c-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="72f0c-116">Insira as cadeias de caracteres do qualificador para cada componente qualificado na coluna qualificador.</span><span class="sxs-lookup"><span data-stu-id="72f0c-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="72f0c-117">Insira uma cadeia de caracteres localizada a ser exibida para o usuário e descrevendo o componente qualificado na coluna opcional AppData.</span><span class="sxs-lookup"><span data-stu-id="72f0c-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="72f0c-118">Uma cadeia de caracteres explicativa deve ser colocada no campo AppData, como "dicionário francês", em vez de apenas o LCID numérico.</span><span class="sxs-lookup"><span data-stu-id="72f0c-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="72f0c-119">Insira o nome do recurso que usa esse componente na \_ coluna recurso.</span><span class="sxs-lookup"><span data-stu-id="72f0c-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="72f0c-120">O identificador de recurso neste campo também deve estar listado na coluna recurso da tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="72f0c-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="72f0c-121">Gere um GUID de categoria para esta categoria de componentes qualificados.</span><span class="sxs-lookup"><span data-stu-id="72f0c-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="72f0c-122">Este deve ser um [GUID](guid.md)válido.</span><span class="sxs-lookup"><span data-stu-id="72f0c-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="72f0c-123">Se você usar um utilitário como o GUIDGEN para gerar o GUID, verifique se ele contém apenas letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="72f0c-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="72f0c-124">Para cada componente qualificado nessa categoria, insira o GUID da categoria no campo ComponentID da [tabela PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="72f0c-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="72f0c-125">O exemplo a seguir ilustra como a categoria "modelos de FAX" de componentes qualificados é criada nas tabelas componente, recurso e PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="72f0c-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="72f0c-126">Tabela PublishComponent</span><span class="sxs-lookup"><span data-stu-id="72f0c-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="72f0c-127">ComponentId</span><span class="sxs-lookup"><span data-stu-id="72f0c-127">ComponentId</span></span>                  | <span data-ttu-id="72f0c-128">Qualificador</span><span class="sxs-lookup"><span data-stu-id="72f0c-128">Qualifier</span></span> | <span data-ttu-id="72f0c-129">AppData</span><span class="sxs-lookup"><span data-stu-id="72f0c-129">AppData</span></span>             | <span data-ttu-id="72f0c-130">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="72f0c-130">Feature\_</span></span>   | <span data-ttu-id="72f0c-131">Componente\_</span><span class="sxs-lookup"><span data-stu-id="72f0c-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="72f0c-132">{GUID de categoria do modelo de FAX}</span><span class="sxs-lookup"><span data-stu-id="72f0c-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="72f0c-133">1046</span><span class="sxs-lookup"><span data-stu-id="72f0c-133">1033</span></span>      | <span data-ttu-id="72f0c-134">Modelo em inglês americano</span><span class="sxs-lookup"><span data-stu-id="72f0c-134">US English template</span></span> | <span data-ttu-id="72f0c-135">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-135">FAXTemplate</span></span> | <span data-ttu-id="72f0c-136">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="72f0c-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="72f0c-137">1041</span><span class="sxs-lookup"><span data-stu-id="72f0c-137">1041</span></span>      | <span data-ttu-id="72f0c-138">Modelo japonês</span><span class="sxs-lookup"><span data-stu-id="72f0c-138">Japanese template</span></span>   | <span data-ttu-id="72f0c-139">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-139">FAXTemplate</span></span> | <span data-ttu-id="72f0c-140">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="72f0c-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="72f0c-141">1054</span><span class="sxs-lookup"><span data-stu-id="72f0c-141">1054</span></span>      | <span data-ttu-id="72f0c-142">Modelo tailandês</span><span class="sxs-lookup"><span data-stu-id="72f0c-142">Thai template</span></span>       | <span data-ttu-id="72f0c-143">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-143">FAXTemplate</span></span> | <span data-ttu-id="72f0c-144">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="72f0c-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="72f0c-145">1031</span><span class="sxs-lookup"><span data-stu-id="72f0c-145">1031</span></span>      | <span data-ttu-id="72f0c-146">Modelo alemão</span><span class="sxs-lookup"><span data-stu-id="72f0c-146">German template</span></span>     | <span data-ttu-id="72f0c-147">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-147">FAXTemplate</span></span> | <span data-ttu-id="72f0c-148">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="72f0c-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="72f0c-149">[Tabela de componentes](component-table.md) (tabela parcial)</span><span class="sxs-lookup"><span data-stu-id="72f0c-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="72f0c-150">Componente</span><span class="sxs-lookup"><span data-stu-id="72f0c-150">Component</span></span>      | <span data-ttu-id="72f0c-151">ComponentId</span><span class="sxs-lookup"><span data-stu-id="72f0c-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="72f0c-152">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="72f0c-152">FAXTemplateENU</span></span> | <span data-ttu-id="72f0c-153">{*Modelo de fax (inglês americano) GUID do componente*}</span><span class="sxs-lookup"><span data-stu-id="72f0c-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="72f0c-154">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="72f0c-154">FAXTemplateJPN</span></span> | <span data-ttu-id="72f0c-155">{*GUID do componente do modelo de fax (japonês)*}</span><span class="sxs-lookup"><span data-stu-id="72f0c-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="72f0c-156">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="72f0c-156">FAXTemplateTHA</span></span> | <span data-ttu-id="72f0c-157">{*GUID do componente do modelo de fax (tailandês)*}</span><span class="sxs-lookup"><span data-stu-id="72f0c-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="72f0c-158">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="72f0c-158">FAXTemplateDEU</span></span> | <span data-ttu-id="72f0c-159">{*GUID do componente do modelo de fax (alemão)*}</span><span class="sxs-lookup"><span data-stu-id="72f0c-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="72f0c-160">[Tabela de recursos](feature-table.md) (tabela parcial)</span><span class="sxs-lookup"><span data-stu-id="72f0c-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="72f0c-161">Recurso</span><span class="sxs-lookup"><span data-stu-id="72f0c-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="72f0c-162">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-162">FAXTemplate</span></span> |
| <span data-ttu-id="72f0c-163">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-163">FAXTemplate</span></span> |
| <span data-ttu-id="72f0c-164">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-164">FAXTemplate</span></span> |
| <span data-ttu-id="72f0c-165">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="72f0c-165">FAXTemplate</span></span> |



 

 

 



