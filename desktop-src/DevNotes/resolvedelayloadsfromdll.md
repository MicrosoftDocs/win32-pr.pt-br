---
description: Encaminha o trabalho na resolução de importações carregadas com atraso do binário pai para um binário de destino.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Função ResolveDelayLoadsFromDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754903"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="a17ea-103">Função ResolveDelayLoadsFromDll</span><span class="sxs-lookup"><span data-stu-id="a17ea-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="a17ea-104">Encaminha o trabalho na resolução de importações carregadas com atraso do binário pai para um binário de destino.</span><span class="sxs-lookup"><span data-stu-id="a17ea-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a17ea-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a17ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a17ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a17ea-107">*ParentBase* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a17ea-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17ea-108">O endereço base do módulo que atrasa a carga de outro binário.</span><span class="sxs-lookup"><span data-stu-id="a17ea-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="a17ea-109">*TargetDllName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a17ea-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17ea-110">O nome da DLL de destino.</span><span class="sxs-lookup"><span data-stu-id="a17ea-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="a17ea-111">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="a17ea-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a17ea-112">Reservado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="a17ea-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a17ea-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a17ea-113">Return value</span></span>

<span data-ttu-id="a17ea-114">O endereço do descritor de carga de atraso, se for encontrado; caso contrário, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a17ea-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a17ea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a17ea-115">Requirements</span></span>



| <span data-ttu-id="a17ea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a17ea-116">Requirement</span></span> | <span data-ttu-id="a17ea-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a17ea-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a17ea-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a17ea-118">Library</span></span><br/> | <dl> <span data-ttu-id="a17ea-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a17ea-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a17ea-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a17ea-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a17ea-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a17ea-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a17ea-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a17ea-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a17ea-123">[Suporte do vinculador para DLLs de Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="a17ea-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




