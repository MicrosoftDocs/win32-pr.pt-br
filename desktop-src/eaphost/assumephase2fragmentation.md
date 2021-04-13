---
title: AssumePhase2Fragmentation
description: A chave do registro AssumePhase2Fragmentation determina se o servidor e o cliente pressupõem a fragmentação da fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365329"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="4d7db-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="4d7db-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="4d7db-104">A chave do registro AssumePhase2Fragmentation determina se o servidor e o cliente pressupõem a fragmentação da fase 2.</span><span class="sxs-lookup"><span data-stu-id="4d7db-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4d7db-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="4d7db-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="4d7db-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d7db-106">Remarks</span></span>

<span data-ttu-id="4d7db-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="4d7db-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="4d7db-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4d7db-108">Value</span></span>   | <span data-ttu-id="4d7db-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d7db-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7db-110">0</span><span class="sxs-lookup"><span data-stu-id="4d7db-110">0</span></span>       | <span data-ttu-id="4d7db-111">Servidor e cliente pressupõe que a outra parte não é capaz de fragmentação da fase 2 durante a autenticação de PEAP.</span><span class="sxs-lookup"><span data-stu-id="4d7db-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="4d7db-112">diferente</span><span class="sxs-lookup"><span data-stu-id="4d7db-112">nonzero</span></span> | <span data-ttu-id="4d7db-113">Servidor e cliente assumem que a outra parte é capaz de fragmentação da fase 2 durante a autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="4d7db-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="4d7db-114">Se esse valor de registro não estiver presente, o servidor e o cliente assumem que a outra parte é capaz da fragmentação da fase 2 durante a autenticação de PEAP.</span><span class="sxs-lookup"><span data-stu-id="4d7db-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d7db-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d7db-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d7db-116">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="4d7db-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




