---
description: O valor da propriedade Resumo do número de revisão no fluxo de informações de resumo deve ser alterado para um valor novo e exclusivo ao localizar um banco de dados, pois o banco de dados de instalação está sendo alterado. Consulte códigos de pacote.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Atualizando um fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370777"
---
# <a name="updating-a-summary-information-stream"></a><span data-ttu-id="43ae8-104">Atualizando um fluxo de informações de resumo</span><span class="sxs-lookup"><span data-stu-id="43ae8-104">Updating a Summary Information Stream</span></span>

<span data-ttu-id="43ae8-105">O valor da propriedade [**Resumo do número de revisão**](revision-number-summary.md) no [fluxo de informações de resumo](summary-information-stream.md) deve ser alterado para um valor novo e exclusivo ao localizar um banco de dados, pois o banco de dados de instalação está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="43ae8-105">The value of the [**Revision Number Summary**](revision-number-summary.md) Property in the [summary information stream](summary-information-stream.md) must be changed to a new, unique value when localizing a database, because the installation database is being changed.</span></span> <span data-ttu-id="43ae8-106">Consulte [códigos de pacote](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="43ae8-106">See [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="43ae8-107">O valor da propriedade de [**Resumo do modelo**](template-summary.md) no fluxo de informações de resumo deve ser alterado para o identificador de idioma numérico (LangID) do novo idioma.</span><span class="sxs-lookup"><span data-stu-id="43ae8-107">The value of the [**Template Summary**](template-summary.md) Property in the summary information stream must be changed to the numeric language identifier (LANGID) of the new language.</span></span>

<span data-ttu-id="43ae8-108">Se as cadeias de caracteres de texto descritivos no fluxo de informações de resumo forem localizadas para o novo idioma, a propriedade de [**Resumo CodePage**](codepage-summary.md) deverá ser definida como a página de código correta para o novo idioma.</span><span class="sxs-lookup"><span data-stu-id="43ae8-108">If the descriptive text strings in the summary information stream are localized to the new language, the [**Codepage Summary**](codepage-summary.md) Property must be set to the correct code page for the new language.</span></span>

<span data-ttu-id="43ae8-109">Você pode modificar o fluxo de informações resumidas do pacote localizado pelo mesmo procedimento que a [adição de informações resumidas](adding-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="43ae8-109">You may modify the summary information stream of the localized package by the same procedure as in [Adding Summary Information](adding-summary-information.md).</span></span> <span data-ttu-id="43ae8-110">Um exemplo que demonstra o uso dos métodos de informações de resumo do banco de dados também é fornecido no SDK do Windows Installer como o WiSumInf.vbs do utilitário.</span><span class="sxs-lookup"><span data-stu-id="43ae8-110">An example demonstrating the use of the database summary information methods is also provided in the Windows Installer SDK as the utility WiSumInf.vbs.</span></span> <span data-ttu-id="43ae8-111">Para obter mais informações sobre WiSumInf.vbs, consulte [gerenciar informações de resumo](manage-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="43ae8-111">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

[<span data-ttu-id="43ae8-112">Continuar</span><span class="sxs-lookup"><span data-stu-id="43ae8-112">Continue</span></span>](adding-localized-resources.md)

 

 



