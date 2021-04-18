---
title: Função DDCCIGetCapabilitiesStringLength
description: Obtém o comprimento de uma cadeia de caracteres de recursos para um monitor.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Configuração do monitor de função DDCCIGetCapabilitiesStringLength
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749808"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="1b7c6-104">Função DDCCIGetCapabilitiesStringLength</span><span class="sxs-lookup"><span data-stu-id="1b7c6-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b7c6-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="1b7c6-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="1b7c6-107">Obtém o comprimento de uma cadeia de caracteres de recursos para um monitor.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b7c6-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="1b7c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b7c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7c6-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b7c6-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7c6-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1b7c6-112">*pdwLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1b7c6-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7c6-113">Recebe o comprimento da cadeia de caracteres de recursos, em caracteres, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7c6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b7c6-114">Return value</span></span>

<span data-ttu-id="1b7c6-115">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="1b7c6-116">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="1b7c6-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b7c6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b7c6-117">Remarks</span></span>

<span data-ttu-id="1b7c6-118">Os aplicativos devem chamar [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="1b7c6-119">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-119">This function has no associated import library.</span></span> <span data-ttu-id="1b7c6-120">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="1b7c6-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b7c6-121">Requirements</span></span>



| <span data-ttu-id="1b7c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b7c6-122">Requirement</span></span> | <span data-ttu-id="1b7c6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1b7c6-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7c6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b7c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7c6-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b7c6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1b7c6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b7c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7c6-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b7c6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1b7c6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1b7c6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b7c6-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b7c6-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b7c6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b7c6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7c6-131">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="1b7c6-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

