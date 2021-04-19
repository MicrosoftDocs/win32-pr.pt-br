---
description: Exemplos de controles dos pais
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Exemplos de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781599"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="feefb-103">Exemplos de controles dos pais</span><span class="sxs-lookup"><span data-stu-id="feefb-103">Parental Controls Samples</span></span>

<span data-ttu-id="feefb-104">O código de exemplo para controles dos pais está disponível em caminho <installation directory> \\ Windows \\ <version number> \\ Samples \\ Security \\ ParentalControls.</span><span class="sxs-lookup"><span data-stu-id="feefb-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="feefb-105">Os exemplos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="feefb-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="feefb-106">Utilitários</span><span class="sxs-lookup"><span data-stu-id="feefb-106">Utilities</span></span>

<span data-ttu-id="feefb-107">Funcionalidade auxiliar para gerenciamento COM básico, operações de cadeia de caracteres de SID e funcionalidade de leitura e gravação do WMI.</span><span class="sxs-lookup"><span data-stu-id="feefb-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="feefb-108">Todos os outros exemplos dependem deste projeto, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="feefb-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="feefb-109">ComplianceAPI</span><span class="sxs-lookup"><span data-stu-id="feefb-109">ComplianceAPI</span></span>

<span data-ttu-id="feefb-110">Aplicativo de console orientado por linha de comando demonstrando como usar a API de conformidade para recuperar um subconjunto de chaves de configurações para um usuário.</span><span class="sxs-lookup"><span data-stu-id="feefb-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="feefb-111">ComplianceApp</span><span class="sxs-lookup"><span data-stu-id="feefb-111">ComplianceApp</span></span>

<span data-ttu-id="feefb-112">Aplicativo de console simples que demonstra o uso da API de conformidade para verificar o registro em log necessário e restrições específicas.</span><span class="sxs-lookup"><span data-stu-id="feefb-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="feefb-113">Se as restrições de tempo estiverem habilitadas, o aplicativo também aguardará os eventos de logout iminentes.</span><span class="sxs-lookup"><span data-stu-id="feefb-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="feefb-114">UIExtensibility</span><span class="sxs-lookup"><span data-stu-id="feefb-114">UIExtensibility</span></span>

<span data-ttu-id="feefb-115">Aplicativo de console orientado por linha de comando demonstrando o uso das APIs do WMI e do esquema WPC para listar, consultar, adicionar, modificar e excluir entradas do link de extensibilidade da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="feefb-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="feefb-116">Exemplo de linha de comando para exemplo:</span><span class="sxs-lookup"><span data-stu-id="feefb-116">Example command line for sample:</span></span>

<span data-ttu-id="feefb-117">"D: \\ WPC \\ Samples \\ Security \\ ParentalControls \\ UIExtensibility \\ debug \\ UIExtensibility" Add/g: {FD59BB7F-54AB-11DB-9666-00E08161165F}/c: 0/N: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-101/S: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-103/I: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-104/D: d:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="feefb-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="feefb-118">em que UiExtRC é uma DLL de recurso simples com recursos de cadeia de caracteres para a ID 101 e 103 e 24x24 pixel 32-bit com Bitmaps alfa para recursos 104 e 106.</span><span class="sxs-lookup"><span data-stu-id="feefb-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="feefb-119">Webextensibility</span><span class="sxs-lookup"><span data-stu-id="feefb-119">WebExtensibility</span></span>

<span data-ttu-id="feefb-120">Aplicativo de console orientado por linha de comando demonstrando como usar as APIs WMI e o esquema WPC para listar, adicionar e excluir entradas de isenção de URL ou aplicativo HTTP e para definir e redefinir uma substituição de filtro de conteúdo da Web com as propriedades Filterid e FilterName.</span><span class="sxs-lookup"><span data-stu-id="feefb-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="feefb-121">O acesso ao aplicativo HTTP somente leitura e às listas de isenção de URL não é mostrado, mas o código para ler as listas seria o mesmo para o caso de leitura/gravação, exceto para a modificação do parâmetro WMI.</span><span class="sxs-lookup"><span data-stu-id="feefb-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



