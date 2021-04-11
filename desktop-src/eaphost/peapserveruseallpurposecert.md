---
title: PeapServerUseAllPurposeCert
description: A chave do registro PeapServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104293624"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="e67ef-103">PeapServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="e67ef-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="e67ef-104">A chave do registro PeapServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="e67ef-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e67ef-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="e67ef-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="e67ef-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e67ef-106">Remarks</span></span>

<span data-ttu-id="e67ef-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e67ef-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="e67ef-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e67ef-108">Value</span></span>        | <span data-ttu-id="e67ef-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e67ef-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e67ef-110">1</span><span class="sxs-lookup"><span data-stu-id="e67ef-110">1</span></span>            | <span data-ttu-id="e67ef-111">Os certificados de uso geral no repositório de certificados do cliente ou do servidor são selecionados para autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="e67ef-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="e67ef-112">Outros valores</span><span class="sxs-lookup"><span data-stu-id="e67ef-112">Other values</span></span> | <span data-ttu-id="e67ef-113">Os certificados de uso insuficiente no repositório de certificados do cliente ou do servidor não são selecionados para autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="e67ef-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="e67ef-114">Se esse valor de registro não estiver presente, os certificados de uso máximo no repositório de certificados do cliente ou do servidor serão selecionados para autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="e67ef-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e67ef-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e67ef-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e67ef-116">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="e67ef-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




