---
title: Nomes de Version-Independent WFP e direcionamento de versões específicas do Windows
description: Em muitos casos, a API da WFP (Windows Filtering Platform) fornece mais de uma versão de uma função ou estrutura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783312"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="6e4da-103">Nomes de Version-Independent WFP e direcionamento de versões específicas do Windows</span><span class="sxs-lookup"><span data-stu-id="6e4da-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="6e4da-104">Em muitos casos, a API da WFP (Windows Filtering Platform) fornece mais de uma versão de uma função ou estrutura.</span><span class="sxs-lookup"><span data-stu-id="6e4da-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="6e4da-105">A maioria dos nomes de função e de dados na API WFP terminam com um número de versão, como "0" ou "1", mesmo se houver apenas uma versão.</span><span class="sxs-lookup"><span data-stu-id="6e4da-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="6e4da-106">Mapeamento de versão em fwpvi. h</span><span class="sxs-lookup"><span data-stu-id="6e4da-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="6e4da-107">O arquivo de cabeçalho fwpvi. h é incluído a partir do SDK do Windows 7 e do WDK.</span><span class="sxs-lookup"><span data-stu-id="6e4da-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="6e4da-108">Esse arquivo de cabeçalho mapeia o nome da API sem versão para a versão apropriada para uso com um determinado sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6e4da-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="6e4da-109">Por exemplo, aqui está um breve trecho da versão do fwpvi. h incluída no SDK do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6e4da-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



<span data-ttu-id="6e4da-110">Como mostrado acima, há apenas uma versão do **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – portanto, qualquer chamada para **FwpmNetEventCreateEnumHandle** sempre chamará **FwpmNetEventCreateEnumHandle0**, independentemente do sistema operacional de destino.</span><span class="sxs-lookup"><span data-stu-id="6e4da-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="6e4da-111">No entanto, há três versões de de **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)e [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span><span class="sxs-lookup"><span data-stu-id="6e4da-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="6e4da-112">O arquivo de cabeçalho fwpvi. h garante que uma chamada para **FwpmNetEventEnum** chamará a versão mais apropriada para o sistema operacional de destino:</span><span class="sxs-lookup"><span data-stu-id="6e4da-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="6e4da-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) para Windows 8 (ou posterior)</span><span class="sxs-lookup"><span data-stu-id="6e4da-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="6e4da-114">O [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) para Windows 7 é direcionado</span><span class="sxs-lookup"><span data-stu-id="6e4da-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="6e4da-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) para sistemas operacionais anteriores (como o Windows Vista ou o Windows Vista com Service Pack 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="6e4da-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="6e4da-116">Chamando funções e estruturas Version-Independent</span><span class="sxs-lookup"><span data-stu-id="6e4da-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="6e4da-117">Os desenvolvedores de WFP destinados a um determinado sistema operacional ou versão do WDK são incentivados a sempre programar em relação às macros independentes de versão.</span><span class="sxs-lookup"><span data-stu-id="6e4da-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="6e4da-118">Isso selecionará automaticamente a versão mais recente com suporte no sistema operacional que você está direcionando.</span><span class="sxs-lookup"><span data-stu-id="6e4da-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="6e4da-119">O uso dos arquivos de cabeçalho mais recentes é recomendado, mesmo quando destinado a um sistema operacional anterior.</span><span class="sxs-lookup"><span data-stu-id="6e4da-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="6e4da-120">Fazer isso de forma consistente garantirá que a versão mais recente com suporte seja usada e também possa facilitar a manutenção e a atualização do código.</span><span class="sxs-lookup"><span data-stu-id="6e4da-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="6e4da-121">A [documentação de referência da API WFP](fwp-reference.md) descreve cada versão de uma API numerada.</span><span class="sxs-lookup"><span data-stu-id="6e4da-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="6e4da-122">Se houver mais de uma versão, o sistema operacional de destino será observado.</span><span class="sxs-lookup"><span data-stu-id="6e4da-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="6e4da-123">No entanto, os desenvolvedores geralmente desejarão chamar as APIs independentes de versão (numéricas) e indicar o sistema operacional de destino (como **NTDDI \_ WIN6** para Windows Vista ou **NTDDI \_ WIN8** para Windows 8).</span><span class="sxs-lookup"><span data-stu-id="6e4da-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="6e4da-124">Para garantir a manipulação adequada das funções que usam parâmetros diferentes em versões diferentes, você pode incluir blocos condicionais, como `#if (NTDDI_VERSION >= NTDDI_WIN7)` .</span><span class="sxs-lookup"><span data-stu-id="6e4da-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




