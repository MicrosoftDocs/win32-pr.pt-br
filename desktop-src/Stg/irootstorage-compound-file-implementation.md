---
title: IRootStorage-implementação de arquivo composto
description: A implementação de arquivo composto do COM do IRootStorage permite que você dê suporte ao salvamento de arquivos em situações de baixa memória ou pouco espaço em disco. Para obter informações sobre como essa interface se comporta, consulte IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637258"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="fa32e-105">IRootStorage-implementação de arquivo composto</span><span class="sxs-lookup"><span data-stu-id="fa32e-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="fa32e-106">A implementação de arquivo composto do COM do [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) permite que você dê suporte ao salvamento de arquivos em situações de baixa memória ou pouco espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="fa32e-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="fa32e-107">Para obter informações sobre como essa interface se comporta, consulte **IRootStorage**.</span><span class="sxs-lookup"><span data-stu-id="fa32e-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fa32e-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="fa32e-108">When to Use</span></span>

<span data-ttu-id="fa32e-109">Use a implementação fornecida pelo sistema do [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) apenas para dar suporte ao salvamento de arquivos em condições de baixa memória.</span><span class="sxs-lookup"><span data-stu-id="fa32e-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa32e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa32e-110">Remarks</span></span>

<span data-ttu-id="fa32e-111">É possível chamar a implementação de COM de [**IRootStorage:: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) para fazer uma operação salvar como normal em outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa32e-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="fa32e-112">No entanto, os aplicativos que fazem isso podem não ser compatíveis com gerações futuras do armazenamento COM.</span><span class="sxs-lookup"><span data-stu-id="fa32e-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="fa32e-113">Para evitar essa possibilidade, os aplicativos que executam uma operação salvar como devem criar manualmente o segundo arquivo composto e invocar [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span><span class="sxs-lookup"><span data-stu-id="fa32e-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="fa32e-114">O método **IRootStorage:: SwitchToFile** deve ser usado somente em situações de emergência (memória insuficiente ou de espaço em disco).</span><span class="sxs-lookup"><span data-stu-id="fa32e-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa32e-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa32e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa32e-116">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="fa32e-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="fa32e-117">**IRootStorage::SwitchToFile**</span><span class="sxs-lookup"><span data-stu-id="fa32e-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




