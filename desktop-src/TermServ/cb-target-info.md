---
title: Estrutura de CB_TARGET_INFO (Cbclient. h)
description: Contém informações sobre o computador de destino e os endereços IP em que as conexões de entrada devem ser redirecionadas.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- Estrutura de CB_TARGET_INFO Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PCB_TARGET_INFO Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369392"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="33e0e-105">Estrutura de informações de \_ destino CB \_</span><span class="sxs-lookup"><span data-stu-id="33e0e-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="33e0e-106">Contém informações sobre o computador de destino e os endereços IP em que as conexões de entrada devem ser redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="33e0e-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="33e0e-107">Essa estrutura é usada com o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="33e0e-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e0e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33e0e-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="33e0e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="33e0e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="33e0e-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="33e0e-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="33e0e-111">Representa o nome de domínio totalmente qualificado do servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="33e0e-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="33e0e-112">Para um cenário de RDV (virtualização de Área de Trabalho Remota), esse membro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="33e0e-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="33e0e-113">Para um cenário de RDSH (host de sessão Área de Trabalho Remota), esse membro contém o nome do servidor em que a conexão de entrada é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="33e0e-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="33e0e-114">**AddressCount**</span><span class="sxs-lookup"><span data-stu-id="33e0e-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="33e0e-115">O número de entradas válidas na matriz de **endereços** .</span><span class="sxs-lookup"><span data-stu-id="33e0e-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="33e0e-116">**Endereços**</span><span class="sxs-lookup"><span data-stu-id="33e0e-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="33e0e-117">Uma matriz de cadeias de caracteres que contêm os endereços IP onde as conexões de entrada são redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="33e0e-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="33e0e-118">O número de elementos válidos nessa matriz é especificado no membro **AddressCount** .</span><span class="sxs-lookup"><span data-stu-id="33e0e-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33e0e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e0e-119">Requirements</span></span>



| <span data-ttu-id="33e0e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e0e-120">Requirement</span></span> | <span data-ttu-id="33e0e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="33e0e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33e0e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e0e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33e0e-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="33e0e-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="33e0e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e0e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33e0e-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33e0e-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="33e0e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33e0e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e0e-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e0e-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e0e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="33e0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e0e-129">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="33e0e-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





