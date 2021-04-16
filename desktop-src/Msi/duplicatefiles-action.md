---
description: A ação DuplicateFiles duplica os arquivos instalados pela ação InstallFiles. Os arquivos duplicados podem ser copiados para o mesmo diretório com um nome diferente ou para um diretório diferente com o nome original.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Ação DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750616"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="2fa2d-104">Ação DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="2fa2d-104">DuplicateFiles Action</span></span>

<span data-ttu-id="2fa2d-105">A ação DuplicateFiles duplica os arquivos instalados pela ação [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa2d-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="2fa2d-106">Os arquivos duplicados podem ser copiados para o mesmo diretório com um nome diferente ou para um diretório diferente com o nome original.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2fa2d-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="2fa2d-107">Sequence Restrictions</span></span>

<span data-ttu-id="2fa2d-108">A ação DuplicateFiles deve vir após a [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="2fa2d-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="2fa2d-109">A ação DuplicateFiles também deve vir após a [ação PatchFiles](patchfiles-action.md) para evitar a duplicação da versão sem patch do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2fa2d-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="2fa2d-110">ActionData Messages</span></span>



| <span data-ttu-id="2fa2d-111">Campo</span><span class="sxs-lookup"><span data-stu-id="2fa2d-111">Field</span></span> | <span data-ttu-id="2fa2d-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="2fa2d-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="2fa2d-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2fa2d-113">\[1\]</span></span> | <span data-ttu-id="2fa2d-114">Identificador de arquivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="2fa2d-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="2fa2d-115">\[6\]</span></span> | <span data-ttu-id="2fa2d-116">Tamanho do arquivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="2fa2d-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="2fa2d-117">\[9\]</span></span> | <span data-ttu-id="2fa2d-118">Identificador do diretório que contém o arquivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2fa2d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fa2d-119">Remarks</span></span>

<span data-ttu-id="2fa2d-120">A ação DuplicateFiles processa uma entrada de [tabela replicafile](duplicatefile-table.md) somente se o componente vinculado a essa entrada estiver sendo instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="2fa2d-121">Para obter mais informações, consulte [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fa2d-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="2fa2d-122">A cadeia de caracteres no campo DestFolder é um nome de propriedade cujo valor deve ser resolvido para um caminho totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="2fa2d-123">Essa propriedade pode ser qualquer uma das entradas de diretório na tabela de [diretório](directory-table.md) , qualquer propriedade de pasta predefinida ([**CommonFilesFolder**](commonfilesfolder.md), por exemplo) ou uma propriedade definida por qualquer entrada na tabela [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa2d-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="2fa2d-124">Se a propriedade **DestFolder** não for avaliada como um caminho válido, a ação DuplicateFiles não fará nada para essa entrada.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="2fa2d-125">Se o nome do arquivo de destino na coluna Destname da tabela Duplicatafile for deixado em branco, o nome do arquivo de destino será o mesmo que o nome do arquivo original.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="2fa2d-126">Os arquivos instalados pela ação DuplicateFiles são removidos pela ação [RemoveDuplicateFiles](removeduplicatefiles-action.md) quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="2fa2d-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



