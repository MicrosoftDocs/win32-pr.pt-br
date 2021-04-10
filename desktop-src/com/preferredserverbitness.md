---
title: PreferredServerBitness
description: Define a arquitetura preferida, 32 bits ou 64 bits, para esse servidor COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- COM valor do registro PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294530"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="89fdd-104">PreferredServerBitness</span><span class="sxs-lookup"><span data-stu-id="89fdd-104">PreferredServerBitness</span></span>

<span data-ttu-id="89fdd-105">Define a arquitetura preferida, 32 bits ou 64 bits, para esse servidor COM.</span><span class="sxs-lookup"><span data-stu-id="89fdd-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="89fdd-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="89fdd-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="89fdd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="89fdd-107">Remarks</span></span>

<span data-ttu-id="89fdd-108">Esse é um valor **reg \_ DWORD** que está disponível apenas nas versões de 64 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="89fdd-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="89fdd-109">Valor</span><span class="sxs-lookup"><span data-stu-id="89fdd-109">Value</span></span> | <span data-ttu-id="89fdd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="89fdd-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89fdd-111">1</span><span class="sxs-lookup"><span data-stu-id="89fdd-111">1</span></span>     | <span data-ttu-id="89fdd-112">Corresponder a arquitetura do servidor à arquitetura do cliente.</span><span class="sxs-lookup"><span data-stu-id="89fdd-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="89fdd-113">Por exemplo, se o cliente for de 32 bits, use uma versão de 32 bits do servidor, se estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="89fdd-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="89fdd-114">Caso contrário, a solicitação de ativação do cliente falhará.</span><span class="sxs-lookup"><span data-stu-id="89fdd-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="89fdd-115">2</span><span class="sxs-lookup"><span data-stu-id="89fdd-115">2</span></span>     | <span data-ttu-id="89fdd-116">Use uma versão de 32 bits do servidor.</span><span class="sxs-lookup"><span data-stu-id="89fdd-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="89fdd-117">Se não houver um, a solicitação de ativação do cliente falhará.</span><span class="sxs-lookup"><span data-stu-id="89fdd-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="89fdd-118">3</span><span class="sxs-lookup"><span data-stu-id="89fdd-118">3</span></span>     | <span data-ttu-id="89fdd-119">Use uma versão de 64 bits do servidor.</span><span class="sxs-lookup"><span data-stu-id="89fdd-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="89fdd-120">Se não houver um, a solicitação de ativação do cliente falhará.</span><span class="sxs-lookup"><span data-stu-id="89fdd-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="89fdd-121">Se esse valor não estiver presente, então:</span><span class="sxs-lookup"><span data-stu-id="89fdd-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="89fdd-122">Se o computador que hospeda o servidor estiver executando o Windows XP ou o Windows Server 2003 sem o SP1 ou posterior instalado, o COM prefere uma versão de 64 bits do servidor, se disponível; caso contrário, ele ativará uma versão de 32 bits do servidor.</span><span class="sxs-lookup"><span data-stu-id="89fdd-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="89fdd-123">Se o computador que hospeda o servidor estiver executando o Windows Server 2003 com SP1 ou posterior instalado, o COM tentará corresponder a arquitetura do servidor à arquitetura do cliente.</span><span class="sxs-lookup"><span data-stu-id="89fdd-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="89fdd-124">Em outras palavras, para um cliente de 32 bits, o COM ativará um servidor de 32 bits, se disponível; caso contrário, ele ativará uma versão de 64 bits do servidor.</span><span class="sxs-lookup"><span data-stu-id="89fdd-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="89fdd-125">Para um cliente de 64 bits, o COM ativará um servidor de 64 bits, se disponível; caso contrário, ele ativará um servidor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="89fdd-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="89fdd-126">O cliente também pode especificar sua própria preferência de arquitetura por meio dos sinalizadores de servidor CLSCTX \_ Activate de \_ 32 \_ bits \_ e CLSCTX \_ Ativar \_ 64 \_ bits \_ , e eles substituirão a preferência do servidor.</span><span class="sxs-lookup"><span data-stu-id="89fdd-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="89fdd-127">Para obter mais informações e um gráfico de possíveis interações entre as preferências de arquitetura do cliente e do servidor, consulte [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span><span class="sxs-lookup"><span data-stu-id="89fdd-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89fdd-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89fdd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89fdd-129">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="89fdd-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 