---
description: A biblioteca de administração do MTS fornecida com as interfaces de administração do COM+ fornece compatibilidade com versões anteriores da biblioteca de administração do MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Biblioteca de administração MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500922"
---
# <a name="mts-administration-library"></a><span data-ttu-id="ccc66-103">Biblioteca de administração MTS</span><span class="sxs-lookup"><span data-stu-id="ccc66-103">MTS Administration Library</span></span>

<span data-ttu-id="ccc66-104">A biblioteca de administração do MTS fornecida com as interfaces de administração do COM+ fornece compatibilidade com versões anteriores da biblioteca de administração do MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="ccc66-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="ccc66-105">O código de administração do MTS 2,0 mais existente ainda funcionará com a biblioteca MTSAdmin fornecida; no entanto, algumas funcionalidades foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="ccc66-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="ccc66-106">Para aproveitar a nova funcionalidade ou se estiver escrevendo o código de Administração pela primeira vez, você deverá usar a biblioteca COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="ccc66-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="ccc66-107">Os seguintes elementos na biblioteca de administração MTS atual são alterados da biblioteca de administração do MTS 2,0:</span><span class="sxs-lookup"><span data-stu-id="ccc66-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="ccc66-108">A interface **IRemoteComponentUtil** não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ccc66-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="ccc66-109">A coleção **RemoteComponents** não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ccc66-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="ccc66-110">A Propriedade RoleID não está mais disponível, o nome da função agora é usado como a chave para isso.</span><span class="sxs-lookup"><span data-stu-id="ccc66-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="ccc66-111">O método **ExportPackage** não exporta mais um client.exe.</span><span class="sxs-lookup"><span data-stu-id="ccc66-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="ccc66-112">A propriedade RemoteComponentInstallPath não é mais exposta na coleção [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc66-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="ccc66-113">A propriedade ApplicationInstallPath não será mais exposta na coleção [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc66-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="ccc66-114">O pacote do sistema agora é chamado de aplicativo do sistema.</span><span class="sxs-lookup"><span data-stu-id="ccc66-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="ccc66-115">O pacote de utilitários agora é chamado de utilitários COM+.</span><span class="sxs-lookup"><span data-stu-id="ccc66-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="ccc66-116">A Propriedade IsSystem existe na coleção de [**componentes**](components.md) em MTSAdmin, mas retornará "NotImpl" Quando marcada e não será salva se estiver definida.</span><span class="sxs-lookup"><span data-stu-id="ccc66-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="ccc66-117">A Propriedade PackageName não tem mais suporte da coleção de [**componentes**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc66-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="ccc66-118">Para descobrir o nome do pacote, agora você precisará obter o PackageID e, em seguida, encontrar o pacote correspondente na coleção de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ccc66-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="ccc66-119">As propriedades a seguir não existem mais na coleção [**InterfacesForComponent**](interfacesforcomponent.md) :</span><span class="sxs-lookup"><span data-stu-id="ccc66-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="ccc66-120">**ProxyCLSID**</span><span class="sxs-lookup"><span data-stu-id="ccc66-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="ccc66-121">**ProxyDLL**</span><span class="sxs-lookup"><span data-stu-id="ccc66-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="ccc66-122">**ProxyThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="ccc66-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="ccc66-123">**TypeLibfile**</span><span class="sxs-lookup"><span data-stu-id="ccc66-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="ccc66-124">**TypeLibid**</span><span class="sxs-lookup"><span data-stu-id="ccc66-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="ccc66-125">**TypeLibLangID**</span><span class="sxs-lookup"><span data-stu-id="ccc66-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="ccc66-126">**TypeLibPlatform**</span><span class="sxs-lookup"><span data-stu-id="ccc66-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="ccc66-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="ccc66-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccc66-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccc66-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc66-129">Conversão automática do MTS</span><span class="sxs-lookup"><span data-stu-id="ccc66-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="ccc66-130">Resultados e problemas de conversão de COM+</span><span class="sxs-lookup"><span data-stu-id="ccc66-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="ccc66-131">Conversão manual do MTS</span><span class="sxs-lookup"><span data-stu-id="ccc66-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



