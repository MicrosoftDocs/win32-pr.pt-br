---
description: Chamado por CertDeleteCTLFromStore antes de excluir uma CTL do repositório.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Função de retorno de chamada CertStoreProvDeleteCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828006"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="16b9e-103">Função de retorno de chamada CertStoreProvDeleteCTL</span><span class="sxs-lookup"><span data-stu-id="16b9e-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="16b9e-104">A função de retorno de chamada **CertStoreProvDeleteCTL** é chamada por [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) antes de excluir uma CTL da loja.</span><span class="sxs-lookup"><span data-stu-id="16b9e-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="16b9e-105">Essa função determina se uma CTL pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="16b9e-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b9e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16b9e-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="16b9e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16b9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b9e-108">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b9e-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b9e-109">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="16b9e-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="16b9e-110">*pCtlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b9e-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b9e-111">Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="16b9e-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16b9e-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b9e-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b9e-113">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="16b9e-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b9e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16b9e-114">Return value</span></span>

<span data-ttu-id="16b9e-115">Retornará **true** se uma CTL puder ser excluída do repositório.</span><span class="sxs-lookup"><span data-stu-id="16b9e-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b9e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b9e-116">Requirements</span></span>



| <span data-ttu-id="16b9e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b9e-117">Requirement</span></span> | <span data-ttu-id="16b9e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="16b9e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16b9e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16b9e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16b9e-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="16b9e-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="16b9e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16b9e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16b9e-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16b9e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
