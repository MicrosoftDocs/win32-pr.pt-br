---
title: Método TestAndSetState da classe Win32_RDSHServer
description: Compara o estado atual com o termo especificado; Se as duas corresponderem, o estado será definido como um novo valor. Independentemente da correspondência, o estado atual também é retornado.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método TestAndSetState
- Método TestAndSetState Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085657"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="b9221-107">Método TestAndSetState da classe Win32 \_ RDSHServer</span><span class="sxs-lookup"><span data-stu-id="b9221-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="b9221-108">Compara o estado atual com o termo especificado; Se as duas corresponderem, o estado será definido como um novo valor.</span><span class="sxs-lookup"><span data-stu-id="b9221-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="b9221-109">Independentemente da correspondência, o estado atual também é retornado.</span><span class="sxs-lookup"><span data-stu-id="b9221-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9221-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9221-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="b9221-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9221-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9221-112">*Termo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9221-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9221-113">Um valor a ser comparado com o estado atual; Se os dois valores corresponderem, o estado será definido como *NewState*.</span><span class="sxs-lookup"><span data-stu-id="b9221-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="b9221-114">*NewState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9221-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9221-115">O novo valor do estado.</span><span class="sxs-lookup"><span data-stu-id="b9221-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="b9221-116">*Initstate* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b9221-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9221-117">Em caso de êxito ou falha, retorna o estado atual.</span><span class="sxs-lookup"><span data-stu-id="b9221-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9221-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9221-118">Requirements</span></span>



| <span data-ttu-id="b9221-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9221-119">Requirement</span></span> | <span data-ttu-id="b9221-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b9221-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9221-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9221-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9221-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b9221-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b9221-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9221-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9221-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b9221-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="b9221-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9221-125">Namespace</span></span><br/>                | <span data-ttu-id="b9221-126">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="b9221-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b9221-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b9221-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9221-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9221-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9221-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b9221-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9221-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9221-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b9221-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9221-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9221-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b9221-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





