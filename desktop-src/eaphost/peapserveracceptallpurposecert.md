---
title: PeapServerAcceptAllPurposeCert
description: A chave do registro PeapServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para a autenticação PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105789615"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="29c88-103">PeapServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="29c88-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="29c88-104">A chave do registro PeapServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para a autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="29c88-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="29c88-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="29c88-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="29c88-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="29c88-106">Remarks</span></span>

<span data-ttu-id="29c88-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="29c88-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="29c88-108">Valor</span><span class="sxs-lookup"><span data-stu-id="29c88-108">Value</span></span>        | <span data-ttu-id="29c88-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="29c88-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c88-110">1</span><span class="sxs-lookup"><span data-stu-id="29c88-110">1</span></span>            | <span data-ttu-id="29c88-111">O servidor e o cliente aceitam certificados com todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="29c88-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="29c88-112">Outros valores</span><span class="sxs-lookup"><span data-stu-id="29c88-112">Other values</span></span> | <span data-ttu-id="29c88-113">O servidor e o cliente não aceitam certificados de todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="29c88-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="29c88-114">Se esse valor de registro não estiver presente, o servidor e o cliente aceitarão os certificados de todas as finalidades enviadas pela outra entidade para autenticação de PEAP.</span><span class="sxs-lookup"><span data-stu-id="29c88-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29c88-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29c88-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29c88-116">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="29c88-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




