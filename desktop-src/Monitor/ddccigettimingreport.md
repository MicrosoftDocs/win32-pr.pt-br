---
title: Função DDCCIGetTimingReport
description: Obtém as frequências de sincronização horizontal e vertical de um monitor.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Configuração do monitor de função DDCCIGetTimingReport
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918422"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="4365b-104">Função DDCCIGetTimingReport</span><span class="sxs-lookup"><span data-stu-id="4365b-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4365b-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4365b-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="4365b-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="4365b-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="4365b-107">Obtém as frequências de sincronização horizontal e vertical de um monitor.</span><span class="sxs-lookup"><span data-stu-id="4365b-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="4365b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4365b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="4365b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4365b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4365b-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4365b-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4365b-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="4365b-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4365b-112">*pmtr* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4365b-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4365b-113">Um ponteiro para uma estrutura de [**\_ \_ relatório de tempo do MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) que recebe as informações de tempo.</span><span class="sxs-lookup"><span data-stu-id="4365b-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4365b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4365b-114">Return value</span></span>

<span data-ttu-id="4365b-115">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="4365b-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="4365b-116">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="4365b-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4365b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4365b-117">Remarks</span></span>

<span data-ttu-id="4365b-118">Os aplicativos devem chamar [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="4365b-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="4365b-119">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="4365b-119">This function has no associated import library.</span></span> <span data-ttu-id="4365b-120">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="4365b-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="4365b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4365b-121">Requirements</span></span>



| <span data-ttu-id="4365b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4365b-122">Requirement</span></span> | <span data-ttu-id="4365b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4365b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4365b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4365b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4365b-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4365b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4365b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4365b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4365b-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4365b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4365b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4365b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4365b-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4365b-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4365b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4365b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4365b-131">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="4365b-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

