---
title: Método ITSRemoteProgram3 ServerStartApp
description: Especifica um aplicativo para iniciar na sessão remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ServerStartApp
- Método ServerStartApp Serviços de Área de Trabalho Remota, interface ITSRemoteProgram3
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram3, método ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788034"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="c723f-106">Método ITSRemoteProgram3:: ServerStartApp</span><span class="sxs-lookup"><span data-stu-id="c723f-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="c723f-107">Especifica um aplicativo para iniciar na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="c723f-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c723f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c723f-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="c723f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c723f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c723f-110">*bstrAppUserModelId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c723f-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c723f-111">*bstrArguments* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c723f-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c723f-112">*vbExpandEnvVarInArgumentsOnServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c723f-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="c723f-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c723f-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="c723f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c723f-114">Return value</span></span>

<span data-ttu-id="c723f-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c723f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c723f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c723f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c723f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c723f-117">Requirements</span></span>



| <span data-ttu-id="c723f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c723f-118">Requirement</span></span> | <span data-ttu-id="c723f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c723f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c723f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c723f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c723f-121">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c723f-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c723f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c723f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c723f-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c723f-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="c723f-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c723f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="c723f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c723f-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c723f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c723f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c723f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c723f-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c723f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c723f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c723f-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="c723f-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





