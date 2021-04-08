---
description: Define a atribuição de conjuntos de CPU selecionados para o thread especificado. Essa atribuição substitui a atribuição padrão do processo, se houver uma definida.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Função SetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828359"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="5d25d-104">Função SetThreadSelectedCpuSets</span><span class="sxs-lookup"><span data-stu-id="5d25d-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="5d25d-105">Define a atribuição de conjuntos de CPU selecionados para o thread especificado.</span><span class="sxs-lookup"><span data-stu-id="5d25d-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="5d25d-106">Essa atribuição substitui a atribuição padrão do processo, se houver uma definida.</span><span class="sxs-lookup"><span data-stu-id="5d25d-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d25d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d25d-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="5d25d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d25d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d25d-109">*Thread* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5d25d-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d25d-110">Especifica o thread no qual definir a atribuição de conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="5d25d-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="5d25d-111">Esse identificador deve ter o \_ direito de \_ acesso de informações limitadas ao conjunto de threads \_ .</span><span class="sxs-lookup"><span data-stu-id="5d25d-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="5d25d-112">O valor retornado por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) também pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="5d25d-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="5d25d-113">*CpuSetIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5d25d-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d25d-114">Especifica a lista de IDs de conjunto de CPU a ser definida como o conjunto de CPU selecionado pelo thread.</span><span class="sxs-lookup"><span data-stu-id="5d25d-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="5d25d-115">Se isso for nulo, a API desmarcará qualquer atribuição, revertendo para processar a atribuição padrão se uma estiver definida.</span><span class="sxs-lookup"><span data-stu-id="5d25d-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="5d25d-116">*CpuSetIdCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5d25d-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d25d-117">Especifica o número de IDs na lista passada no argumento **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="5d25d-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="5d25d-118">Se esse valor for nulo, ele deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="5d25d-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d25d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d25d-119">Return value</span></span>

<span data-ttu-id="5d25d-120">Essa função não pode falhar quando passaram parâmetros válidos.</span><span class="sxs-lookup"><span data-stu-id="5d25d-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d25d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d25d-121">Requirements</span></span>



| <span data-ttu-id="5d25d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d25d-122">Requirement</span></span> | <span data-ttu-id="5d25d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5d25d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d25d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d25d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d25d-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="5d25d-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="5d25d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d25d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d25d-127">Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5d25d-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="5d25d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d25d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d25d-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d25d-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="5d25d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d25d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d25d-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d25d-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="5d25d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5d25d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d25d-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d25d-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
