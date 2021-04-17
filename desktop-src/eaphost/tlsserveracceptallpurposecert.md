---
title: TlsServerAcceptAllPurposeCert
description: A chave do registro TlsServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para autenticação EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105749183"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="63fbe-103">TlsServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="63fbe-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="63fbe-104">A chave do registro TlsServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="63fbe-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="63fbe-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="63fbe-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="63fbe-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="63fbe-106">Remarks</span></span>

<span data-ttu-id="63fbe-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63fbe-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="63fbe-108">Valor</span><span class="sxs-lookup"><span data-stu-id="63fbe-108">Value</span></span>        | <span data-ttu-id="63fbe-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="63fbe-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63fbe-110">1</span><span class="sxs-lookup"><span data-stu-id="63fbe-110">1</span></span>            | <span data-ttu-id="63fbe-111">O servidor e o cliente aceitam certificados com todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="63fbe-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="63fbe-112">Outros valores</span><span class="sxs-lookup"><span data-stu-id="63fbe-112">Other values</span></span> | <span data-ttu-id="63fbe-113">O servidor e o cliente não aceitam certificados de todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="63fbe-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="63fbe-114">Se esse valor de registro não estiver presente, o servidor e o cliente aceitarão os certificados de todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="63fbe-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63fbe-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63fbe-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63fbe-116">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="63fbe-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




