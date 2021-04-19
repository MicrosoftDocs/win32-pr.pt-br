---
description: Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.
title: Função DlpGetEnforcementApiVersion (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495360"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="c4a61-103">Função DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="c4a61-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="c4a61-104">Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="c4a61-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a61-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4a61-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="c4a61-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4a61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a61-107">*MajorVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4a61-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a61-108">Um **DWORD** especificando o número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="c4a61-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c4a61-109">*MajorVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4a61-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a61-110">Um **DWORD** especificando o número de versão secundária.</span><span class="sxs-lookup"><span data-stu-id="c4a61-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c4a61-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4a61-111">Return value</span></span>

<span data-ttu-id="c4a61-112">Retorna um HRESULT que inclui, mas não se limita a, os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4a61-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="c4a61-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c4a61-113">HRESULT</span></span> | <span data-ttu-id="c4a61-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4a61-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="c4a61-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4a61-115">S_OK</span></span> | <span data-ttu-id="c4a61-116">A função foi concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="c4a61-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="c4a61-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4a61-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c4a61-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a61-118">Requirements</span></span>



| <span data-ttu-id="c4a61-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a61-119">Requirement</span></span>          |    <span data-ttu-id="c4a61-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c4a61-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a61-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a61-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a61-122">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c4a61-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c4a61-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c4a61-123">DLL</span></span><br/>                      | <span data-ttu-id="c4a61-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c4a61-124">EndpointDlp.dll</span></span> |