---
title: TLS_HANDLE
description: Representa um identificador para um servidor de licença Área de Trabalho Remota.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644453"
---
# <a name="tls_handle"></a><span data-ttu-id="fa464-104">identificador de TLS \_</span><span class="sxs-lookup"><span data-stu-id="fa464-104">TLS\_HANDLE</span></span>

<span data-ttu-id="fa464-105">Representa um identificador para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="fa464-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="fa464-106">Esse identificador é retornado pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="fa464-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="fa464-107">Este tipo de dados não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="fa464-107">This data type has no associated header file.</span></span> <span data-ttu-id="fa464-108">Para usá-lo, você deve defini-lo por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="fa464-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="fa464-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa464-109">Requirements</span></span>



| <span data-ttu-id="fa464-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa464-110">Requirement</span></span> | <span data-ttu-id="fa464-111">Valor</span><span class="sxs-lookup"><span data-stu-id="fa464-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fa464-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa464-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fa464-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa464-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fa464-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa464-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fa464-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa464-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa464-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fa464-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa464-117">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="fa464-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="fa464-118">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="fa464-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





