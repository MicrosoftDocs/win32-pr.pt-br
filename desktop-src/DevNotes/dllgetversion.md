---
description: A função DllGetVersion recupera o número de versão de Cabinet.dll usando a estrutura CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Função DllGetVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751586"
---
# <a name="dllgetversion-function"></a><span data-ttu-id="9c20f-103">Função DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="9c20f-103">DllGetVersion function</span></span>

<span data-ttu-id="9c20f-104">\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.\]</span><span class="sxs-lookup"><span data-stu-id="9c20f-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="9c20f-105">A função **DllGetVersion** recupera o número de versão de Cabinet.dll usando a estrutura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9c20f-105">The **DllGetVersion** function retrieves the version number of Cabinet.dll using the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c20f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c20f-106">Syntax</span></span>


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a><span data-ttu-id="9c20f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c20f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c20f-108">*pcdvi*</span><span class="sxs-lookup"><span data-stu-id="9c20f-108">*pcdvi*</span></span> 
</dt> <dd>

<span data-ttu-id="9c20f-109">Ponteiro para a estrutura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) que contém as informações de versão.</span><span class="sxs-lookup"><span data-stu-id="9c20f-109">Pointer to the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure that contains the version information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c20f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c20f-110">Return value</span></span>

<span data-ttu-id="9c20f-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9c20f-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c20f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c20f-112">Remarks</span></span>

<span data-ttu-id="9c20f-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9c20f-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c20f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c20f-114">Requirements</span></span>



| <span data-ttu-id="9c20f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c20f-115">Requirement</span></span> | <span data-ttu-id="9c20f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9c20f-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c20f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9c20f-117">DLL</span></span><br/> | <dl> <span data-ttu-id="9c20f-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c20f-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c20f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c20f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c20f-120">**CABINETDLLVERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="9c20f-120">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md)
</dt> <dt>

[<span data-ttu-id="9c20f-121">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="9c20f-121">**GetDllVersion**</span></span>](getdllversion.md)
</dt> </dl>

 

 
