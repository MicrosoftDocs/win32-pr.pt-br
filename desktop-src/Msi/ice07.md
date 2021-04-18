---
description: ICE07 valida que o pacote de instalação especifica que as fontes sejam instaladas no FontsFolder. Se uma fonte for instalada em uma pasta que não seja a FontsFolder, o instalador criará um atalho em vez de realmente instalar a fonte.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750004"
---
# <a name="ice07"></a><span data-ttu-id="07930-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="07930-104">ICE07</span></span>

<span data-ttu-id="07930-105">ICE07 valida que o pacote de instalação especifica que as fontes sejam instaladas no FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="07930-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="07930-106">Se uma fonte for instalada em uma pasta que não seja a FontsFolder, o instalador criará um atalho em vez de realmente instalar a fonte.</span><span class="sxs-lookup"><span data-stu-id="07930-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="07930-107">A ação personalizada ICE07 faz o seguinte para cada fonte na [tabela de fontes](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="07930-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="07930-108">Localiza o arquivo de fonte ao qual o título de cada fonte pertence usando a [tabela de fontes](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="07930-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="07930-109">Consulta a \_ coluna componente da [tabela de arquivos](file-table.md) do componente que controla cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="07930-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="07930-110">Consulta a \_ coluna Directory da [tabela de componentes](component-table.md) para obter uma chave na tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="07930-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="07930-111">Resolve a tabela de [diretórios](directory-table.md) para determinar o nome da pasta na qual o instalador deve instalar o arquivo de fonte</span><span class="sxs-lookup"><span data-stu-id="07930-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="07930-112">Posta um erro se o arquivo de fonte está sendo instalado em uma pasta que não seja a FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="07930-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="07930-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="07930-113">Result</span></span>

<span data-ttu-id="07930-114">ICE07 posta um erro se descobrir que o banco de dados especifica que um arquivo de fonte seja instalado em uma pasta que não seja a FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="07930-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="07930-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="07930-115">Example</span></span>

<span data-ttu-id="07930-116">IC07 publicaria a seguinte mensagem de erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="07930-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="07930-117">Tabela de fontes</span><span class="sxs-lookup"><span data-stu-id="07930-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="07930-118">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="07930-118">File\_</span></span> | <span data-ttu-id="07930-119">FontTitle</span><span class="sxs-lookup"><span data-stu-id="07930-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="07930-120">Myrtle</span><span class="sxs-lookup"><span data-stu-id="07930-120">Myrtle</span></span> | <span data-ttu-id="07930-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="07930-121">Tahoma</span></span>    |



 

<span data-ttu-id="07930-122">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="07930-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="07930-123">Arquivo</span><span class="sxs-lookup"><span data-stu-id="07930-123">File</span></span>   | <span data-ttu-id="07930-124">Componente\_</span><span class="sxs-lookup"><span data-stu-id="07930-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="07930-125">Myrtle</span><span class="sxs-lookup"><span data-stu-id="07930-125">Myrtle</span></span> | <span data-ttu-id="07930-126">\_Praia Myrtle</span><span class="sxs-lookup"><span data-stu-id="07930-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="07930-127">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="07930-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="07930-128">Componente</span><span class="sxs-lookup"><span data-stu-id="07930-128">Component</span></span>     | <span data-ttu-id="07930-129">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="07930-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="07930-130">\_Praia Myrtle</span><span class="sxs-lookup"><span data-stu-id="07930-130">Myrtle\_Beach</span></span> | <span data-ttu-id="07930-131">SandBar</span><span class="sxs-lookup"><span data-stu-id="07930-131">SandBar</span></span>     |



 

<span data-ttu-id="07930-132">Neste exemplo, a fonte Tahoma é mapeada para o arquivo de fonte Myrtle.</span><span class="sxs-lookup"><span data-stu-id="07930-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="07930-133">O arquivo Myrtle pertence ao componente Myrtle \_ praia.</span><span class="sxs-lookup"><span data-stu-id="07930-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="07930-134">A resolução da tabela de diretórios mostra que todos os arquivos pertencentes à \_ praia Myrtle devem ser instalados na pasta Sandbar.</span><span class="sxs-lookup"><span data-stu-id="07930-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="07930-135">Como esse não é o FontsFolder, o ICE07 posta uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="07930-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="07930-136">Observe que, se o componente Myrtle da \_ praia realmente pertence à pasta Sandbar, e não ao FontsFolder, a fonte Tahoma pode não pertencer a Myrtle \_ praia.</span><span class="sxs-lookup"><span data-stu-id="07930-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="07930-137">Uma possível correção para o erro seria incluir Tahoma em outro componente que é instalado no diretório FontsFolder</span><span class="sxs-lookup"><span data-stu-id="07930-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07930-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07930-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07930-139">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="07930-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



