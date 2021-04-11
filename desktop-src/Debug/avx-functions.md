---
description: Funções do Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: Funções AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163900"
---
# <a name="avx-functions"></a><span data-ttu-id="aa1bf-103">Funções AVX</span><span class="sxs-lookup"><span data-stu-id="aa1bf-103">AVX Functions</span></span>

<span data-ttu-id="aa1bf-104">A seguir estão as funções do Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="aa1bf-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa1bf-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aa1bf-105">In this section</span></span>



| <span data-ttu-id="aa1bf-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="aa1bf-106">Topic</span></span>                                                                   | <span data-ttu-id="aa1bf-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa1bf-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa1bf-108">**CopyContext**</span><span class="sxs-lookup"><span data-stu-id="aa1bf-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="aa1bf-109">Copia uma estrutura de contexto de origem (incluindo qualquer XState) em uma estrutura de contexto de destino inicializada.</span><span class="sxs-lookup"><span data-stu-id="aa1bf-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="aa1bf-110">**GetEnabledXStateFeatures**</span><span class="sxs-lookup"><span data-stu-id="aa1bf-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="aa1bf-111">Obtém uma máscara de recursos de XState habilitados em processadores x86 ou x64.</span><span class="sxs-lookup"><span data-stu-id="aa1bf-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="aa1bf-112">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="aa1bf-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="aa1bf-113">Retorna a máscara dos recursos do XState definidos em uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .</span><span class="sxs-lookup"><span data-stu-id="aa1bf-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="aa1bf-114">**InitializeContext**</span><span class="sxs-lookup"><span data-stu-id="aa1bf-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="aa1bf-115">Inicializa uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) dentro de um buffer com o tamanho e o alinhamento necessários.</span><span class="sxs-lookup"><span data-stu-id="aa1bf-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="aa1bf-116">**LocateXStateFeature**</span><span class="sxs-lookup"><span data-stu-id="aa1bf-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="aa1bf-117">Recupera um ponteiro para o estado do processador para um recurso XState dentro de uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="aa1bf-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="aa1bf-118">**SetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="aa1bf-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="aa1bf-119">Define a máscara dos recursos do XState definidos em uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="aa1bf-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




