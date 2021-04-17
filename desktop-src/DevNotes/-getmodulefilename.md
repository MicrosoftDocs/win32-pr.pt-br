---
description: Obtém o caminho do módulo.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: Função _GetModuleFileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749654"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="2e0c0-103">\_Função GetModuleFileName</span><span class="sxs-lookup"><span data-stu-id="2e0c0-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="2e0c0-104">\[Essa função é um wrapper sobre a função **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="2e0c0-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="2e0c0-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="2e0c0-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="2e0c0-106">Os aplicativos devem chamar **GetModuleFileName** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="2e0c0-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="2e0c0-107">Obtém o caminho do módulo.</span><span class="sxs-lookup"><span data-stu-id="2e0c0-107">Gets the module path.</span></span> <span data-ttu-id="2e0c0-108">Consulte [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span><span class="sxs-lookup"><span data-stu-id="2e0c0-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0c0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e0c0-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="2e0c0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e0c0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0c0-111">*...*</span><span class="sxs-lookup"><span data-stu-id="2e0c0-111">*...*</span></span> 
<span data-ttu-id="2e0c0-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2e0c0-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2e0c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e0c0-113">Requirements</span></span>



| <span data-ttu-id="2e0c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0c0-114">Requirement</span></span> | <span data-ttu-id="2e0c0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2e0c0-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0c0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2e0c0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="2e0c0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e0c0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0c0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e0c0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0c0-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="2e0c0-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
