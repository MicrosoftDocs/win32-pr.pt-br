---
title: Função GetPhysicalMonitorDescription
description: Obtém uma descrição de um monitor físico.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Configuração do monitor de função GetPhysicalMonitorDescription
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085523"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="9a79b-104">Função GetPhysicalMonitorDescription</span><span class="sxs-lookup"><span data-stu-id="9a79b-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a79b-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a79b-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="9a79b-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="9a79b-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="9a79b-107">Obtém uma descrição de um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="9a79b-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a79b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a79b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="9a79b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a79b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a79b-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a79b-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a79b-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="9a79b-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9a79b-112">*dwPhysicalMonitorDescriptionSizeInChars* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a79b-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a79b-113">O número de caracteres na matriz *szPhysicalMonitorDescription* .</span><span class="sxs-lookup"><span data-stu-id="9a79b-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="9a79b-114">*szPhysicalMonitorDescription* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9a79b-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a79b-115">Um ponteiro para uma matriz que recebe a descrição.</span><span class="sxs-lookup"><span data-stu-id="9a79b-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="9a79b-116">O número de elementos na matriz deve ser pelo menos o **\_ tamanho da \_ Descrição \_ do monitor físico**.</span><span class="sxs-lookup"><span data-stu-id="9a79b-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a79b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a79b-117">Return value</span></span>

<span data-ttu-id="9a79b-118">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="9a79b-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9a79b-119">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="9a79b-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a79b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a79b-120">Remarks</span></span>

<span data-ttu-id="9a79b-121">Em vez de usar essa função, os aplicativos devem chamar uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="9a79b-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="9a79b-122">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="9a79b-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="9a79b-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="9a79b-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="9a79b-124">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="9a79b-124">This function has no associated import library.</span></span> <span data-ttu-id="9a79b-125">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9a79b-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a79b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a79b-126">Requirements</span></span>



| <span data-ttu-id="9a79b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a79b-127">Requirement</span></span> | <span data-ttu-id="9a79b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9a79b-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9a79b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a79b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9a79b-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a79b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9a79b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a79b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9a79b-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a79b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9a79b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9a79b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a79b-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a79b-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a79b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a79b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a79b-136">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="9a79b-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

