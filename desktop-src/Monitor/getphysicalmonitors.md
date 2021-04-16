---
title: Função GetPhysicalMonitors
description: Obtém os monitores físicos associados a um dispositivo de vídeo.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configuração do monitor de função GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750829"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="d5b19-104">Função GetPhysicalMonitors</span><span class="sxs-lookup"><span data-stu-id="d5b19-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5b19-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5b19-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="d5b19-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="d5b19-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="d5b19-107">Obtém os monitores físicos associados a um dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5b19-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b19-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5b19-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="d5b19-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5b19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b19-110">*pstrDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5b19-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b19-111">Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d5b19-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="d5b19-112">*dwPhysicalMonitorArraySize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5b19-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b19-113">O número de elementos na matriz *pdwNumPhysicalMonitorHandlesInArray* .</span><span class="sxs-lookup"><span data-stu-id="d5b19-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="d5b19-114">Para obter o tamanho necessário da matriz, chame [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span><span class="sxs-lookup"><span data-stu-id="d5b19-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5b19-115">*pdwNumPhysicalMonitorHandlesInArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5b19-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b19-116">Recebe o número de itens que a função copia para a matriz *phPhysicalMonitorArray* .</span><span class="sxs-lookup"><span data-stu-id="d5b19-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="d5b19-117">*phPhysicalMonitorArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5b19-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b19-118">Uma matriz que recebe identificadores para os monitores físicos.</span><span class="sxs-lookup"><span data-stu-id="d5b19-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="d5b19-119">Cada identificador deve ser liberado chamando [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span><span class="sxs-lookup"><span data-stu-id="d5b19-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5b19-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5b19-120">Return value</span></span>

<span data-ttu-id="d5b19-121">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="d5b19-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d5b19-122">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="d5b19-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b19-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5b19-123">Remarks</span></span>

<span data-ttu-id="d5b19-124">Em vez de usar essa função, os aplicativos devem chamar uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="d5b19-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="d5b19-125">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="d5b19-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="d5b19-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="d5b19-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="d5b19-127">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="d5b19-127">This function has no associated import library.</span></span> <span data-ttu-id="d5b19-128">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d5b19-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b19-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5b19-129">Requirements</span></span>



| <span data-ttu-id="d5b19-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5b19-130">Requirement</span></span> | <span data-ttu-id="d5b19-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d5b19-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b19-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5b19-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b19-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5b19-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d5b19-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5b19-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b19-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5b19-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d5b19-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d5b19-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5b19-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5b19-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5b19-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5b19-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b19-139">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="d5b19-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

