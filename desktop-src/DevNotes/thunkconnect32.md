---
description: A função ThunkConnect32 é usada por drivers de dispositivo de 16 bits (para MS-DOS) que chamam o kernel de 32 bits.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: Função ThunkConnect32
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747903"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="34eeb-103">Função ThunkConnect32</span><span class="sxs-lookup"><span data-stu-id="34eeb-103">ThunkConnect32 function</span></span>

<span data-ttu-id="34eeb-104">\[Essa função foi suportada para compatibilidade com versões anteriores, mas não está presente nas versões atuais do Windows.</span><span class="sxs-lookup"><span data-stu-id="34eeb-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="34eeb-105">Os novos drivers de dispositivo devem ser 32 ou 64 bits e não precisam dessa função.\]</span><span class="sxs-lookup"><span data-stu-id="34eeb-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="34eeb-106">A função **ThunkConnect32** é usada por drivers de dispositivo de 16 bits (para MS-dos) que chamam o kernel de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="34eeb-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="34eeb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34eeb-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="34eeb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34eeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34eeb-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="34eeb-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="34eeb-110">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="34eeb-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="34eeb-112">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="34eeb-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="34eeb-114">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="34eeb-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="34eeb-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="34eeb-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="34eeb-118">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-119">*dwReason*</span><span class="sxs-lookup"><span data-stu-id="34eeb-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="34eeb-120">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34eeb-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34eeb-121">Return value</span></span>

<span data-ttu-id="34eeb-122">Sempre retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="34eeb-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="34eeb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34eeb-123">Requirements</span></span>



| <span data-ttu-id="34eeb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="34eeb-124">Requirement</span></span> | <span data-ttu-id="34eeb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="34eeb-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34eeb-126">DLL</span><span class="sxs-lookup"><span data-stu-id="34eeb-126">DLL</span></span><br/> | <dl> <span data-ttu-id="34eeb-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34eeb-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




