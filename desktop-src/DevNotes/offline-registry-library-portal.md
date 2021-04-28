---
description: Biblioteca de registro offline
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Biblioteca de registro offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089244"
---
# <a name="offline-registry-library"></a><span data-ttu-id="583cb-103">Biblioteca de registro offline</span><span class="sxs-lookup"><span data-stu-id="583cb-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="583cb-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="583cb-104">Purpose</span></span>

<span data-ttu-id="583cb-105">A biblioteca de registro offline (Offreg.dll) é usada para modificar um hive do registro fora do registro do sistema ativo.</span><span class="sxs-lookup"><span data-stu-id="583cb-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="583cb-106">Essa biblioteca destina-se a cenários de atualização de registro, como manutenção de uma imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="583cb-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="583cb-107">A biblioteca dá suporte aos formatos do hive do registro a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="583cb-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="583cb-108">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="583cb-108">Developer audience</span></span>

<span data-ttu-id="583cb-109">Essa tecnologia é para OEMs (fabricantes de equipamento original), fornecedores de software antivírus e antimalware e outros desenvolvedores de aplicativos que devem ser capazes de analisar arquivos do hive do registro sem carregá-los no registro ativo.</span><span class="sxs-lookup"><span data-stu-id="583cb-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="583cb-110">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="583cb-110">Run-time requirements</span></span>

<span data-ttu-id="583cb-111">A biblioteca de registro offline é fornecida como uma DLL (biblioteca de vínculo dinâmico) redistribuível binária.</span><span class="sxs-lookup"><span data-stu-id="583cb-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="583cb-112">Essa biblioteca é executada nas seguintes versões do Windows:</span><span class="sxs-lookup"><span data-stu-id="583cb-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="583cb-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="583cb-113">Windows Server 2016</span></span>  
<span data-ttu-id="583cb-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="583cb-114">Windows 10</span></span>  
<span data-ttu-id="583cb-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="583cb-115">Windows 8.1</span></span>  
<span data-ttu-id="583cb-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="583cb-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="583cb-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="583cb-117">Windows 8</span></span>  
<span data-ttu-id="583cb-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="583cb-118">Windows Server 2012</span></span>  
<span data-ttu-id="583cb-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="583cb-119">Windows 7</span></span>  
<span data-ttu-id="583cb-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="583cb-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="583cb-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="583cb-121">Windows Server 2008</span></span>  
<span data-ttu-id="583cb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="583cb-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="583cb-123">Os aplicativos devem ser vinculados a Offreg.dll usando vinculação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="583cb-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="583cb-124">O Offreg.dll é fornecido no Windows Driver Kit (WDK) para Windows 10 e versões anteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="583cb-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="583cb-125">Para obter informações sobre como obter o WDK, consulte [como obter o WDK e o WLK](/windows-hardware/drivers/download-the-wdk) ou visite o site de [assinaturas do MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="583cb-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="583cb-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="583cb-126">In this section</span></span>

-   [<span data-ttu-id="583cb-127">**Sobre a biblioteca de registro offline**</span><span class="sxs-lookup"><span data-stu-id="583cb-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="583cb-128">**Funções da biblioteca do registro offline**</span><span class="sxs-lookup"><span data-stu-id="583cb-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
