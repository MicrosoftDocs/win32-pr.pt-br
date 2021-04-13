---
title: Estrutura de CB_CONNECTION_INFO (Cbclient. h)
description: Contém informações sobre uma solicitação de conexão de entrada.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- Estrutura de CB_CONNECTION_INFO Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PCB_CONNECTION_INFO Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369393"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="4d0c7-105">Estrutura de informações de \_ conexão CB \_</span><span class="sxs-lookup"><span data-stu-id="4d0c7-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="4d0c7-106">Contém informações sobre uma solicitação de conexão de entrada.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="4d0c7-107">Essa estrutura é usada com o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4d0c7-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d0c7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d0c7-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="4d0c7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4d0c7-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d0c7-110">**UserName**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-111">O nome do usuário que está solicitando uma sessão.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-112">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-113">O nome do domínio do qual o **nome de usuário** é membro.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-114">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-115">O caminho totalmente qualificado e o nome de arquivo do programa inicial que é iniciado quando a sessão é iniciada.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="4d0c7-116">Defina esse membro como uma cadeia de caracteres vazia se nenhum programa inicial precisar ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-117">**Recurso**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-118">Um valor da enumeração [**do \_ \_ tipo de recurso CB**](cb-resource-type.md) que especifica o tipo de recurso ao qual a conexão de entrada está se conectando.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="4d0c7-119">Se o membro **pluginname** for **nulo**, esse membro será usado pelo agente de conexão de área de trabalho remota para determinar qual plug-in invocar para determinar o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-121">O nome do plug-in a ser invocado para determinar o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="4d0c7-122">Se esse parâmetro for **NULL**, o membro de **recurso** será usado para determinar qual plug-in invocar.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-123">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-124">O nome do farm que contém os computadores, um dos quais será o computador de destino em que a conexão será redirecionada.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-125">**dwVendorInfoLength**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-126">Este membro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4d0c7-127">**pVendorSpecificInfo**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4d0c7-128">Este membro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4d0c7-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d0c7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d0c7-129">Requirements</span></span>



| <span data-ttu-id="4d0c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d0c7-130">Requirement</span></span> | <span data-ttu-id="4d0c7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4d0c7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d0c7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d0c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4d0c7-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4d0c7-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="4d0c7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d0c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4d0c7-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d0c7-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="4d0c7-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d0c7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d0c7-137"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d0c7-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d0c7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d0c7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d0c7-139">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="4d0c7-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





