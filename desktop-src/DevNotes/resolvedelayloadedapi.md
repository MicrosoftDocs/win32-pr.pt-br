---
description: Localiza a função de destino da importação especificada e substitui o ponteiro de função na conversão de importação pelo destino da implementação da função.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Função ResolveDelayLoadedAPI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749407"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="65f11-103">Função ResolveDelayLoadedAPI</span><span class="sxs-lookup"><span data-stu-id="65f11-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="65f11-104">Localiza a função de destino da importação especificada e substitui o ponteiro de função na conversão de importação pelo destino da implementação da função.</span><span class="sxs-lookup"><span data-stu-id="65f11-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f11-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65f11-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="65f11-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65f11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f11-107">*ParentModuleBase* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65f11-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f11-108">O endereço da base do módulo que importa uma função carregada com atraso.</span><span class="sxs-lookup"><span data-stu-id="65f11-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="65f11-109">*DelayloadDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65f11-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f11-110">O descritor do módulo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="65f11-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="65f11-111">*FailureDllHook* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65f11-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65f11-112">O endereço do gancho de falha.</span><span class="sxs-lookup"><span data-stu-id="65f11-112">The address of the failure hook.</span></span> <span data-ttu-id="65f11-113">Consulte [**DelayLoadFailureHook**](delayloadfailurehook.md).</span><span class="sxs-lookup"><span data-stu-id="65f11-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="65f11-114">*FailureSystemHook* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65f11-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65f11-115">O endereço do gancho de falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="65f11-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="65f11-116">*ThunkAddress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65f11-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65f11-117">Os dados de conversão para a função de destino.</span><span class="sxs-lookup"><span data-stu-id="65f11-117">The thunk data for the target function.</span></span> <span data-ttu-id="65f11-118">Usado para localizar a entrada da tabela de nome específico da função.</span><span class="sxs-lookup"><span data-stu-id="65f11-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="65f11-119">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="65f11-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="65f11-120">Reservado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="65f11-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f11-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65f11-121">Return value</span></span>

<span data-ttu-id="65f11-122">O endereço da importação ou o stub de falha para ele.</span><span class="sxs-lookup"><span data-stu-id="65f11-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f11-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f11-123">Requirements</span></span>



| <span data-ttu-id="65f11-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f11-124">Requirement</span></span> | <span data-ttu-id="65f11-125">Valor</span><span class="sxs-lookup"><span data-stu-id="65f11-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65f11-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65f11-126">Library</span></span><br/> | <dl> <span data-ttu-id="65f11-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="65f11-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65f11-128">DLL</span><span class="sxs-lookup"><span data-stu-id="65f11-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="65f11-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f11-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f11-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="65f11-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="65f11-131">[Suporte do vinculador para DLLs de Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="65f11-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




