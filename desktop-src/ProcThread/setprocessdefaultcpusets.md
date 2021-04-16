---
description: Define a atribuição de conjuntos de CPU padrão para threads no processo especificado. Os threads criados, que não têm conjuntos de CPU definidos explicitamente usando SetThreadSelectedCpuSets, herdarão os conjuntos especificados por SetProcessDefaultCpuSets automaticamente.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Função SetProcessDefaultCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757742"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="4061e-104">Função SetProcessDefaultCpuSets</span><span class="sxs-lookup"><span data-stu-id="4061e-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="4061e-105">Define a atribuição de conjuntos de CPU padrão para threads no processo especificado.</span><span class="sxs-lookup"><span data-stu-id="4061e-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="4061e-106">Os threads criados, que não têm conjuntos de CPU definidos explicitamente usando [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), herdarão os conjuntos especificados por **SetProcessDefaultCpuSets** automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4061e-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="4061e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4061e-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="4061e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4061e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4061e-109">*Processo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4061e-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4061e-110">Especifica o processo para o qual definir os conjuntos de CPU padrão.</span><span class="sxs-lookup"><span data-stu-id="4061e-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="4061e-111">Esse identificador deve ter o \_ direito de \_ acesso definir informações limitadas \_ do processo.</span><span class="sxs-lookup"><span data-stu-id="4061e-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="4061e-112">O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="4061e-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="4061e-113">*CpuSetIds* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4061e-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4061e-114">Especifica a lista de IDs de conjunto de CPU a ser definida como o conjunto de CPU padrão do processo.</span><span class="sxs-lookup"><span data-stu-id="4061e-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="4061e-115">Se isso for nulo, o **SetProcessDefaultCpuSets** desmarcará qualquer atribuição.</span><span class="sxs-lookup"><span data-stu-id="4061e-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="4061e-116">*CpuSetIdCound* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4061e-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4061e-117">Especifica o número de IDs na lista passada no argumento **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="4061e-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="4061e-118">Se esse valor for nulo, ele deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="4061e-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4061e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4061e-119">Return value</span></span>

<span data-ttu-id="4061e-120">Essa função não pode falhar quando passaram parâmetros válidos.</span><span class="sxs-lookup"><span data-stu-id="4061e-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="4061e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4061e-121">Requirements</span></span>



| <span data-ttu-id="4061e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4061e-122">Requirement</span></span> | <span data-ttu-id="4061e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4061e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4061e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4061e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4061e-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="4061e-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="4061e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4061e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4061e-127">Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4061e-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="4061e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4061e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4061e-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4061e-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="4061e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4061e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4061e-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="4061e-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="4061e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4061e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4061e-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4061e-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
