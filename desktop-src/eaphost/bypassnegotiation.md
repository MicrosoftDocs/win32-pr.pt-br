---
title: BypassNegotiation
description: A chave do registro BypassNegotiation determina se as capacidades de negociação entre o servidor e o cliente ocorrem ou se as configurações pré-configuradas são usadas.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365347"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="b7486-103">BypassNegotiation</span><span class="sxs-lookup"><span data-stu-id="b7486-103">BypassNegotiation</span></span>

<span data-ttu-id="b7486-104">A chave do registro BypassNegotiation determina se as capacidades de negociação entre o servidor e o cliente ocorrem ou se as configurações pré-configuradas são usadas.</span><span class="sxs-lookup"><span data-stu-id="b7486-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b7486-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="b7486-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="b7486-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7486-106">Remarks</span></span>

<span data-ttu-id="b7486-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b7486-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="b7486-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b7486-108">Value</span></span>   | <span data-ttu-id="b7486-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7486-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7486-110">0</span><span class="sxs-lookup"><span data-stu-id="b7486-110">0</span></span>       | <span data-ttu-id="b7486-111">Servidor e cliente negociam recursos EAP.</span><span class="sxs-lookup"><span data-stu-id="b7486-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="b7486-112">diferente</span><span class="sxs-lookup"><span data-stu-id="b7486-112">nonzero</span></span> | <span data-ttu-id="b7486-113">O servidor e o cliente não negociam os recursos EAP.</span><span class="sxs-lookup"><span data-stu-id="b7486-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="b7486-114">Servidor e cliente usam o valor da chave do registro [AssumePhase2Fragmentation](assumephase2fragmentation.md) para encontrar os recursos da outra parte.</span><span class="sxs-lookup"><span data-stu-id="b7486-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="b7486-115">Se esse valor de registro não estiver presente, o servidor e o cliente negociarão os recursos EAP..</span><span class="sxs-lookup"><span data-stu-id="b7486-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7486-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7486-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7486-117">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7486-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




