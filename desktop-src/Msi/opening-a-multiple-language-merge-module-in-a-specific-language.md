---
description: Ao mesclar um módulo em um banco de dados de instalação, há dois idiomas importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Abrindo um módulo de mesclagem Multiple-Language em um idioma específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010628"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="d0b67-103">Abrindo um módulo de mesclagem Multiple-Language em um idioma específico</span><span class="sxs-lookup"><span data-stu-id="d0b67-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="d0b67-104">Ao mesclar um módulo em um banco de dados de instalação, há dois idiomas importantes.</span><span class="sxs-lookup"><span data-stu-id="d0b67-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="d0b67-105">O primeiro é o idioma do pacote de instalação de destino especificado por [**ProductLanguage**](productlanguage.md) na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0b67-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="d0b67-106">A segunda é o idioma do módulo de mesclagem que aparece na coluna Language da [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0b67-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="d0b67-107">O idioma do pacote de instalação pode ser passado para o módulo pela ferramenta de mesclagem quando o pacote é aberto para uma mesclagem.</span><span class="sxs-lookup"><span data-stu-id="d0b67-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="d0b67-108">No entanto, às vezes pode ser necessário desconsiderar o idioma do destino e solicitar que o módulo seja aberto em outro idioma, por exemplo, um pacote em inglês instalando os recursos em inglês e alemão do módulo.</span><span class="sxs-lookup"><span data-stu-id="d0b67-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="d0b67-109">Ao abrir um módulo com uma solicitação de idioma, a ferramenta de mesclagem verifica o idioma solicitado em relação aos idiomas especificados na coluna idioma da [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0b67-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="d0b67-110">O processo a seguir é usado para determinar qual idioma usar.</span><span class="sxs-lookup"><span data-stu-id="d0b67-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="d0b67-111">**Para determinar qual idioma usar**</span><span class="sxs-lookup"><span data-stu-id="d0b67-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="d0b67-112">Se o idioma na [tabela ModuleSignature](modulesignature-table.md) for igual ou mais geral do que o idioma solicitado, o módulo será aberto.</span><span class="sxs-lookup"><span data-stu-id="d0b67-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="d0b67-113">Se o módulo der suporte ao idioma exato solicitado, esse idioma será usado.</span><span class="sxs-lookup"><span data-stu-id="d0b67-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="d0b67-114">Se o módulo der suporte ao grupo de idiomas do idioma solicitado que o grupo de idiomas é usado, por exemplo, marque 9 se 1033 foi solicitado, mas não foi encontrado na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d0b67-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="d0b67-115">Verifique se há uma transformação de idioma que altere o módulo para neutro.</span><span class="sxs-lookup"><span data-stu-id="d0b67-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="d0b67-116">Se nenhuma das etapas anteriores for bem-sucedida, o módulo não oferecerá suporte ao idioma solicitado e a mesclagem falhará.</span><span class="sxs-lookup"><span data-stu-id="d0b67-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



