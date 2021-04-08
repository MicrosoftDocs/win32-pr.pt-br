---
title: Função GetNumberOfPhysicalMonitors
description: Obtém o número de monitores físicas associados a um dispositivo de vídeo.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configuração do monitor de função GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824384"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="ee14b-104">Função GetNumberOfPhysicalMonitors</span><span class="sxs-lookup"><span data-stu-id="ee14b-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee14b-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ee14b-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="ee14b-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="ee14b-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="ee14b-107">Obtém o número de monitores físicas associados a um dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ee14b-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee14b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee14b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="ee14b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee14b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee14b-110">*pstrDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee14b-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee14b-111">Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ee14b-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="ee14b-112">*pdwNumberOfPhysicalMonitors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee14b-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee14b-113">Recebe o número de monitores físicos.</span><span class="sxs-lookup"><span data-stu-id="ee14b-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee14b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee14b-114">Return value</span></span>

<span data-ttu-id="ee14b-115">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="ee14b-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ee14b-116">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="ee14b-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee14b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee14b-117">Remarks</span></span>

<span data-ttu-id="ee14b-118">Em vez de usar essa função, os aplicativos devem chamar uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="ee14b-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="ee14b-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="ee14b-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="ee14b-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="ee14b-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="ee14b-121">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="ee14b-121">This function has no associated import library.</span></span> <span data-ttu-id="ee14b-122">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ee14b-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee14b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee14b-123">Requirements</span></span>



| <span data-ttu-id="ee14b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee14b-124">Requirement</span></span> | <span data-ttu-id="ee14b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ee14b-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee14b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee14b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ee14b-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee14b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ee14b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee14b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ee14b-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee14b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ee14b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ee14b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee14b-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee14b-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee14b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee14b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee14b-133">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="ee14b-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

