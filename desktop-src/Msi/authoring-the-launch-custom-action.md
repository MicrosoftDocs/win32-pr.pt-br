---
description: O código-fonte para uma ação personalizada de exemplo chamada Launch, que atende às especificações de exemplo, é fornecido pelo SDK do Windows Installer como o arquivo tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Criando a ação personalizada de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921488"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="14546-103">Criando a ação personalizada de inicialização</span><span class="sxs-lookup"><span data-stu-id="14546-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="14546-104">O código-fonte para uma ação personalizada de exemplo chamada Launch, que atende às especificações de exemplo, é fornecido pelo SDK do Windows Installer como o arquivo tutorial. cpp.</span><span class="sxs-lookup"><span data-stu-id="14546-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="14546-105">Essa ação personalizada faz uso de [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para formatar uma cadeia de caracteres que contém propriedades.</span><span class="sxs-lookup"><span data-stu-id="14546-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="14546-106">A propriedade \[ \# FileKey é \] resolvida para o caminho completo do arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="14546-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="14546-107">Use o arquivo de origem para criar o arquivo Tutorial.dll.</span><span class="sxs-lookup"><span data-stu-id="14546-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="14546-108">O ponto de entrada para essa DLL é LaunchTutorial.</span><span class="sxs-lookup"><span data-stu-id="14546-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="14546-109">A inicialização da ação personalizada de exemplo chama uma DLL escrita em C++ e é gerada a partir de um fluxo binário temporário.</span><span class="sxs-lookup"><span data-stu-id="14546-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="14546-110">As ações personalizadas desse tipo incluem as constantes de tipo base msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData, que fornecem um tipo numérico de base igual a 1.</span><span class="sxs-lookup"><span data-stu-id="14546-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="14546-111">Consulte [tipo de ação personalizada 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="14546-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="14546-112">Como as especificações exigem que a instalação continue se a ação personalizada falhar, a inicialização também incluirá a constante opcional **msidbCustomActionTypeContinue**, que é 64.</span><span class="sxs-lookup"><span data-stu-id="14546-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="14546-113">Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="14546-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="14546-114">O tipo numérico total de inicialização é 65.</span><span class="sxs-lookup"><span data-stu-id="14546-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="14546-115">Continue a [Adicionar Launch às tabelas CustomAction e binary](adding-launch-to-the-customaction-and-binary-tables.md).</span><span class="sxs-lookup"><span data-stu-id="14546-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 



