---
description: HKLM \\ software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646464"
---
# <a name="exec"></a><span data-ttu-id="4107e-103">Exec</span><span class="sxs-lookup"><span data-stu-id="4107e-103">Exec</span></span>

<span data-ttu-id="4107e-104">**HKLM \\ software \\ extensões do Microsoft \\ Internet Explorer \\ \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="4107e-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="4107e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4107e-105">Data type</span></span> | <span data-ttu-id="4107e-106">Intervalo</span><span class="sxs-lookup"><span data-stu-id="4107e-106">Range</span></span>                    | <span data-ttu-id="4107e-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="4107e-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="4107e-108">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="4107e-108">REG\_SZ</span></span>   | <span data-ttu-id="4107e-109">*Caminho para o executável*</span><span class="sxs-lookup"><span data-stu-id="4107e-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="4107e-110">Etapas de integração do navegador</span><span class="sxs-lookup"><span data-stu-id="4107e-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="4107e-111">Use a função [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para determinar se o diagnóstico de rede está instalado.</span><span class="sxs-lookup"><span data-stu-id="4107e-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="4107e-112">Se estiver instalado, a chave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** estará presente.</span><span class="sxs-lookup"><span data-stu-id="4107e-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="4107e-113">Use a função [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para recuperar o caminho do arquivo executável de diagnóstico de rede da entrada **exec** .</span><span class="sxs-lookup"><span data-stu-id="4107e-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="4107e-114">Exibir a nova página de erro se o diagnóstico estiver instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="4107e-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="4107e-115">Crie uma extensão de navegador que cria um item de barra de ferramentas padrão se o diagnóstico estiver instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="4107e-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="4107e-116">Execute o executável de diagnóstico de rede usando o caminho recuperado na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="4107e-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4107e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4107e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4107e-118">Visão geral do recurso ferramentas de diagnóstico de rede</span><span class="sxs-lookup"><span data-stu-id="4107e-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
