---
title: Função DDCCISetVCPFeature
description: Define o valor de um código de VCP (painel de controle virtual) para um monitor.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configuração do monitor de função DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085524"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="ff483-104">Função DDCCISetVCPFeature</span><span class="sxs-lookup"><span data-stu-id="ff483-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff483-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff483-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="ff483-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="ff483-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="ff483-107">Define o valor de um código de VCP (painel de controle virtual) para um monitor.</span><span class="sxs-lookup"><span data-stu-id="ff483-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff483-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff483-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="ff483-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff483-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff483-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff483-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff483-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="ff483-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ff483-112">*dwVCPCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff483-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff483-113">O código VCP a ser definido.</span><span class="sxs-lookup"><span data-stu-id="ff483-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="ff483-114">*dwNewValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff483-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff483-115">O valor do código VCP.</span><span class="sxs-lookup"><span data-stu-id="ff483-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff483-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff483-116">Return value</span></span>

<span data-ttu-id="ff483-117">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="ff483-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ff483-118">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="ff483-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff483-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff483-119">Remarks</span></span>

<span data-ttu-id="ff483-120">Os aplicativos devem chamar [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="ff483-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="ff483-121">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="ff483-121">This function has no associated import library.</span></span> <span data-ttu-id="ff483-122">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ff483-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff483-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff483-123">Requirements</span></span>



| <span data-ttu-id="ff483-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff483-124">Requirement</span></span> | <span data-ttu-id="ff483-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ff483-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff483-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff483-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff483-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff483-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ff483-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff483-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff483-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff483-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff483-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ff483-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff483-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff483-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff483-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ff483-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff483-133">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="ff483-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

