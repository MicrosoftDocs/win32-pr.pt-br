---
title: A MSAA não está disponível para aplicativos da Windows Store
description: A MSAA não está disponível para aplicativos da Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008501"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="0cc4e-103">A MSAA não está disponível para aplicativos da Windows Store</span><span class="sxs-lookup"><span data-stu-id="0cc4e-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="0cc4e-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="0cc4e-104">Platform</span></span>

<span data-ttu-id="0cc4e-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="0cc4e-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="0cc4e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cc4e-106">Description</span></span>

<span data-ttu-id="0cc4e-107">O Windows 8 não oferece suporte a MSAA (Microsoft Acessibilidade Ativa) para ler ou automatizar dados acessíveis de aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="0cc4e-108">A API de automação da interface do usuário (UIA), disponível desde o Windows 7, deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="0cc4e-109">Como não há nenhum recurso existente do aplicativo da Windows Store, não há nenhuma implementação existente afetada por essa alteração.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="0cc4e-110">Isso afeta apenas os novos aplicativos e recursos escritos para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="0cc4e-111">Os desenvolvedores ainda podem usar a MSAA para expor seus dados de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="0cc4e-112">Se os dados MSAA forem fornecidos pelo provedor de aplicativos da Windows Store, os clientes UIA ainda poderão ler e automatizar os dados.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="0cc4e-113">Para simplificar a API para aplicativos da Windows 8Windows Store, decidimos dar suporte apenas à automação da interface do usuário como um cliente para esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="0cc4e-114">Os clientes UIA podem ler provedores UIA nativamente, sem tradução.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="0cc4e-115">Os clientes UIA podem ler provedores de MSAA como convertidos por meio do proxy UIA-to-MSAA.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="0cc4e-116">Isso reduzirá a carga de teste para os desenvolvedores de aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="0cc4e-117">A eliminação do suporte para provedores de MSAA reduziria ainda mais a matriz de testes, mas há aplicativos principais que ainda são baseados em MSAA e não queremos renderizá-los inacessíveis.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0cc4e-118">Manifestação</span><span class="sxs-lookup"><span data-stu-id="0cc4e-118">Manifestation</span></span>

<span data-ttu-id="0cc4e-119">Os desenvolvedores de aplicativos da Windows Store não poderão acessar os detalhes do MSAA no modelo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="0cc4e-120">Solução</span><span class="sxs-lookup"><span data-stu-id="0cc4e-120">Solution</span></span>

<span data-ttu-id="0cc4e-121">Nenhum novo caso automatizado deve ser criado no MSAA para recursos dos aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="0cc4e-122">Alterne qualquer ferramenta interna existente que use MSAA para UIA se precisar interagir com aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="0cc4e-123">Os desenvolvedores de aplicativos da Windows Store devem usar a API de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0cc4e-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="0cc4e-124">Recursos</span><span class="sxs-lookup"><span data-stu-id="0cc4e-124">Resources</span></span>

-   [<span data-ttu-id="0cc4e-125">Conceitos básicos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0cc4e-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 