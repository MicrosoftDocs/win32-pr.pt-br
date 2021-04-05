---
title: Tipos de dados do serviço de acesso remoto (RAS. h)
description: Os tipos de dados a seguir são usados pela API do serviço de acesso remoto.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918415"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="9665c-105">Tipos de dados do serviço de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="9665c-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="9665c-106">Os tipos de dados a seguir são usados pela API do serviço de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="9665c-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="9665c-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="9665c-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="9665c-108">Um [**em \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) que contém um endereço IPv4.</span><span class="sxs-lookup"><span data-stu-id="9665c-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="9665c-109">Com suporte no Windows Vista ou em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="9665c-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="9665c-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="9665c-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="9665c-111">Um [**\_ end In6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) que contém um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="9665c-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="9665c-112">Com suporte no Windows Vista ou em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="9665c-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9665c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9665c-113">Requirements</span></span>



| <span data-ttu-id="9665c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9665c-114">Requirement</span></span> | <span data-ttu-id="9665c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9665c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9665c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9665c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9665c-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9665c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9665c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9665c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9665c-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9665c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9665c-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9665c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9665c-121"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="9665c-121"><dt>Ras.h</dt></span></span> </dl> |



 

