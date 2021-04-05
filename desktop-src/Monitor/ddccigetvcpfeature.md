---
title: Função DDCCIGetVCPFeature
description: Obtém o valor atual, o valor máximo e o tipo de código de um código de painel de controle virtual (VCP) para um monitor.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configuração do monitor de função DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918421"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="6dc93-104">Função DDCCIGetVCPFeature</span><span class="sxs-lookup"><span data-stu-id="6dc93-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6dc93-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dc93-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="6dc93-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="6dc93-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="6dc93-107">Obtém o valor atual, o valor máximo e o tipo de código de um código de painel de controle virtual (VCP) para um monitor.</span><span class="sxs-lookup"><span data-stu-id="6dc93-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dc93-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="6dc93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dc93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dc93-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc93-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="6dc93-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6dc93-112">*dwVCPCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc93-113">O código VCP a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="6dc93-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="6dc93-114">*PVCT* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc93-115">Recebe o tipo de código VCP, como um membro da enumeração de [**\_ tipo de \_ código \_ do MC VCP**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) .</span><span class="sxs-lookup"><span data-stu-id="6dc93-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6dc93-116">*pdwCurrentValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc93-117">Recebe o valor atual do código VCP.</span><span class="sxs-lookup"><span data-stu-id="6dc93-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="6dc93-118">*pdwMaximumValue* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc93-119">Recebe o valor máximo do código VCP.</span><span class="sxs-lookup"><span data-stu-id="6dc93-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dc93-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dc93-120">Return value</span></span>

<span data-ttu-id="6dc93-121">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="6dc93-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="6dc93-122">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="6dc93-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dc93-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dc93-123">Remarks</span></span>

<span data-ttu-id="6dc93-124">Os aplicativos devem chamar [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="6dc93-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="6dc93-125">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="6dc93-125">This function has no associated import library.</span></span> <span data-ttu-id="6dc93-126">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="6dc93-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc93-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dc93-127">Requirements</span></span>



| <span data-ttu-id="6dc93-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dc93-128">Requirement</span></span> | <span data-ttu-id="6dc93-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6dc93-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc93-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dc93-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc93-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6dc93-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dc93-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc93-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6dc93-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6dc93-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6dc93-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dc93-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dc93-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc93-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dc93-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc93-137">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="6dc93-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

