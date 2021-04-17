---
description: Carrega uma biblioteca.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: Função _LoadLibrary
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748518"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="a12c8-103">\_Função LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="a12c8-103">\_LoadLibrary function</span></span>

<span data-ttu-id="a12c8-104">\[Essa função é um wrapper sobre a função **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="a12c8-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="a12c8-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="a12c8-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="a12c8-106">Os aplicativos devem chamar **LoadLibrary** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="a12c8-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="a12c8-107">Carrega uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a12c8-107">Loads a library.</span></span> <span data-ttu-id="a12c8-108">Consulte [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="a12c8-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="a12c8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a12c8-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="a12c8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a12c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12c8-111">*...*</span><span class="sxs-lookup"><span data-stu-id="a12c8-111">*...*</span></span> 
<span data-ttu-id="a12c8-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a12c8-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a12c8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a12c8-113">Requirements</span></span>



| <span data-ttu-id="a12c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12c8-114">Requirement</span></span> | <span data-ttu-id="a12c8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a12c8-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12c8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a12c8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a12c8-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a12c8-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12c8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a12c8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12c8-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="a12c8-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
