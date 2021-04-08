---
description: ICEM13 verifica se o módulo de mesclagem não contém a política do Publicador e os assemblies de configuração.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828032"
---
# <a name="icem13"></a><span data-ttu-id="707bb-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="707bb-103">ICEM13</span></span>

<span data-ttu-id="707bb-104">ICEM13 verifica se o módulo de mesclagem não contém a política do Publicador e os assemblies de configuração.</span><span class="sxs-lookup"><span data-stu-id="707bb-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="707bb-105">Os assemblies de política e configuração do Publicador não devem ser incluídos em módulos de mesclagem destinados para redistribuição porque isso pode afetar outros aplicativos no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="707bb-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="707bb-106">Esse ICEM está disponível no arquivo Mergemod. Cub fornecido no SDK do Windows Installer 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="707bb-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="707bb-107">Para obter detalhes, consulte [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="707bb-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="707bb-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="707bb-108">Result</span></span>

<span data-ttu-id="707bb-109">ICEM13 posta uma mensagem de aviso se encontrar um componente especificado no campo componente da [tabela MsiAssembly](msiassembly-table.md) do módulo de mesclagem que seja uma política do Publicador ou um assembly de configuração.</span><span class="sxs-lookup"><span data-stu-id="707bb-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="707bb-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="707bb-110">Example</span></span>

<span data-ttu-id="707bb-111">ICEM13 lança a seguinte mensagem de aviso se encontrar uma linha na [tabela MsiAssembly](msiassembly-table.md) com um componente ' \[ 1 \] ' especificado no campo de componente que é uma política de editor ou assembly de configuração que foi incluído no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="707bb-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="707bb-112">É possível instalar a política do Publicador e os assemblies de configuração usando o Windows Installer, não é recomendável que esses assemblies sejam redistribuídos nos módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="707bb-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="707bb-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="707bb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="707bb-114">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="707bb-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



