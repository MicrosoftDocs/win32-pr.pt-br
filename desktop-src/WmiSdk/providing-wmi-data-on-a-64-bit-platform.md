---
description: Scripts e aplicativos escritos para sistemas operacionais de 32 bits devem continuar sendo executados corretamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fornecendo dados do WMI em uma plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502220"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="4aeb8-103">Fornecendo dados do WMI em uma plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="4aeb8-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="4aeb8-104">Scripts e aplicativos escritos para sistemas operacionais de 32 bits devem continuar sendo executados corretamente.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="4aeb8-105">Se você tiver um provedor de 32 bits existente, poderá avaliar se precisa gravar uma versão de 64 bits para a operação lado a lado.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="4aeb8-106">Em geral, ambas as versões não são necessárias e a versão de 64 bits pode atender a clientes locais ou remotos de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="4aeb8-107">No entanto, para o modo de compatibilidade de aplicativos de 32 bits, use seu provedor WMI de 32 bits existente em um sistema de 64 bits que é executado no modo WOW64 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="4aeb8-108">Em situações raras, os provedores de 32 bits e de 64 bits devem ser executados lado a lado em sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="4aeb8-109">Nesse caso, a versão apropriada do provedor que é carregada depende se o chamador é de 32 bits ou de 64 bits e local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="4aeb8-110">Um chamador que usa os sinalizadores de contexto de objeto de conexão, **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture**, pode solicitar que o WMI carregue um provedor não padrão.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="4aeb8-111">Para obter mais informações, consulte [obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4aeb8-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="4aeb8-112">No caso incomum de você precisar executar os provedores de 32 bits e de 64 bits lado a lado, você deve garantir que os cenários de instalação e desinstalação sejam tratados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="4aeb8-113">Isso ocorre porque o WMI tem apenas um [*repositório*](gloss-w.md) e as versões de 32 bits e 64 bits do [**mofcomp.exe**](mofcomp.md) colocam os dados no mesmo repositório; Não há nenhuma distinção entre um arquivo. mof de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="4aeb8-114">A reinstalação de uma versão do provedor não afetará: os arquivos. mof serão compilados e as classes armazenadas no repositório.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="4aeb8-115">No entanto, uma segunda desinstalação que exclui um namespace pode interferir na operação do outro provedor.</span><span class="sxs-lookup"><span data-stu-id="4aeb8-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aeb8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4aeb8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aeb8-117">Obter e fornecer dados em um computador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="4aeb8-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="4aeb8-118">Solicitando dados WMI em uma plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="4aeb8-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="4aeb8-119">Fornecendo dados ao WMI</span><span class="sxs-lookup"><span data-stu-id="4aeb8-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



