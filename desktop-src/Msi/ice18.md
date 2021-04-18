---
description: ICE18 valida que todos os diretórios vazios usados como um caminho de chave para um componente são listados na tabela CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770376"
---
# <a name="ice18"></a><span data-ttu-id="00c6d-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="00c6d-103">ICE18</span></span>

<span data-ttu-id="00c6d-104">ICE18 valida que todos os diretórios vazios usados como um caminho de chave para um componente são listados na [tabela CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="00c6d-105">Se a coluna KeyPath da [tabela de componentes](component-table.md) for nula, isso significará que o diretório listado na \_ coluna diretório é o caminho de chave para esse componente.</span><span class="sxs-lookup"><span data-stu-id="00c6d-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="00c6d-106">Como as pastas criadas pelo instalador são excluídas quando se tornam vazias, essa pasta deve estar listada na [tabela CreateFolder](createfolder-table.md) para impedir que o instalador tente instalar todas as vezes.</span><span class="sxs-lookup"><span data-stu-id="00c6d-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="00c6d-107">Não torne o diretório SystemFolder o caminho de chave de um componente.</span><span class="sxs-lookup"><span data-stu-id="00c6d-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="00c6d-108">Como essa pasta está presente em todos os sistemas operacionais, o instalador sempre detecta o caminho da chave se o componente está presente ou não.</span><span class="sxs-lookup"><span data-stu-id="00c6d-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="00c6d-109">Nesse caso, o caminho da chave deve ser um arquivo, uma entrada do registro ou uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="00c6d-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="00c6d-110">Ao executar um ICE18 de validação, primeiro verifique se os itens a seguir estão todos verdadeiros:</span><span class="sxs-lookup"><span data-stu-id="00c6d-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="00c6d-111">A coluna KeyPath da [tabela de componentes](component-table.md) contém um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="00c6d-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="00c6d-112">Que não há arquivos listados para o componente na tabela de [arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="00c6d-113">Que não há arquivos para o componente listado na [tabela removerfile](removefile-table.md) e que o valor em DirProperty seja o mesmo que a \_ coluna Directory da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="00c6d-114">Que não há arquivos para o componente listado na [tabela duplicatefile](duplicatefile-table.md) e que o valor em DestFolder seja o mesmo da \_ coluna Directory da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="00c6d-115">Que não há arquivos para o componente listado na [tabela MoveFile](movefile-table.md) e que o valor em DestFolder é o mesmo que a \_ coluna Directory da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="00c6d-116">Se todos forem verdadeiros, o ICE18 validará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="00c6d-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="00c6d-117">Se a \_ coluna Component da [tabela CreateFolder](createfolder-table.md) tem o mesmo valor que a coluna Component da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="00c6d-118">Se a \_ coluna Directory da tabela CreateFolder tem o mesmo valor que a coluna Directory \_ da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="00c6d-119">Resultado</span><span class="sxs-lookup"><span data-stu-id="00c6d-119">Result</span></span>

<span data-ttu-id="00c6d-120">ICE18 posta uma mensagem de erro se o pacote de instalação especifica um diretório como o caminho da chave para o componente que não está listado na [tabela CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="00c6d-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00c6d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00c6d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c6d-122">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="00c6d-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



