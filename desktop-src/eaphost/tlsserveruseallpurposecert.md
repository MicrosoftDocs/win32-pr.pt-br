---
title: TlsServerUseAllPurposeCert
description: A chave do registro TlsServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104293617"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="8269d-103">TlsServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="8269d-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="8269d-104">A chave do registro TlsServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="8269d-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8269d-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="8269d-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="8269d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="8269d-106">Remarks</span></span>

<span data-ttu-id="8269d-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8269d-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="8269d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8269d-108">Value</span></span>        | <span data-ttu-id="8269d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8269d-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8269d-110">1</span><span class="sxs-lookup"><span data-stu-id="8269d-110">1</span></span>            | <span data-ttu-id="8269d-111">Os certificados de uso geral no repositório de certificados do cliente ou do servidor são selecionados para autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="8269d-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="8269d-112">Outros valores</span><span class="sxs-lookup"><span data-stu-id="8269d-112">Other values</span></span> | <span data-ttu-id="8269d-113">Os certificados de uso insuficiente no repositório de certificados do cliente ou do servidor não são selecionados para autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="8269d-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="8269d-114">Se esse valor de registro não estiver presente, os certificados de uso máximo no repositório de certificados do cliente ou do servidor serão selecionados para autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="8269d-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8269d-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8269d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8269d-116">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="8269d-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




