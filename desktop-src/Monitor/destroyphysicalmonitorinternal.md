---
title: Função DestroyPhysicalMonitorInternal
description: Fecha um identificador para um monitor físico.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Configuração do monitor de função DestroyPhysicalMonitorInternal
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824385"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="16c59-104">Função DestroyPhysicalMonitorInternal</span><span class="sxs-lookup"><span data-stu-id="16c59-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16c59-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="16c59-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="16c59-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="16c59-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="16c59-107">Fecha um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="16c59-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c59-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16c59-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="16c59-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16c59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c59-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16c59-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c59-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="16c59-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c59-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16c59-112">Return value</span></span>

<span data-ttu-id="16c59-113">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="16c59-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="16c59-114">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="16c59-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c59-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="16c59-115">Remarks</span></span>

<span data-ttu-id="16c59-116">Os aplicativos devem chamar [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="16c59-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="16c59-117">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="16c59-117">This function has no associated import library.</span></span> <span data-ttu-id="16c59-118">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="16c59-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c59-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c59-119">Requirements</span></span>



| <span data-ttu-id="16c59-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c59-120">Requirement</span></span> | <span data-ttu-id="16c59-121">Valor</span><span class="sxs-lookup"><span data-stu-id="16c59-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16c59-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16c59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16c59-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16c59-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="16c59-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16c59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16c59-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16c59-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="16c59-126">DLL</span><span class="sxs-lookup"><span data-stu-id="16c59-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c59-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16c59-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c59-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="16c59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c59-129">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="16c59-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

