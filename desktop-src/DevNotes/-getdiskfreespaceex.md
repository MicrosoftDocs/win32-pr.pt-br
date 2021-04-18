---
description: Obtém o espaço livre em disco.
ms.assetid: 4b7f4938-9918-4625-b28d-faf22de56976
title: Função _GetDiskFreeSpaceEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetDiskFreeSpaceEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
ms.openlocfilehash: da4a8eefabf03f6330ac9c1f135482f27dd8aa18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750529"
---
# <a name="_getdiskfreespaceex-function"></a><span data-ttu-id="16e8d-103">\_Função GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="16e8d-103">\_GetDiskFreeSpaceEx function</span></span>

<span data-ttu-id="16e8d-104">\[Essa função é um wrapper sobre a função **GetDiskFreeSpaceEx** .</span><span class="sxs-lookup"><span data-stu-id="16e8d-104">\[This function is a wrapper over the **GetDiskFreeSpaceEx** function.</span></span> <span data-ttu-id="16e8d-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="16e8d-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="16e8d-106">Os aplicativos devem chamar **GetDiskFreeSpaceEx** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="16e8d-106">Applications should call **GetDiskFreeSpaceEx** directly.\]</span></span>

<span data-ttu-id="16e8d-107">Obtém o espaço livre em disco.</span><span class="sxs-lookup"><span data-stu-id="16e8d-107">Gets the free disk space.</span></span> <span data-ttu-id="16e8d-108">Consulte [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span><span class="sxs-lookup"><span data-stu-id="16e8d-108">See [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="16e8d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16e8d-109">Syntax</span></span>


```C++
BOOL _GetDiskFreeSpaceEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="16e8d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16e8d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e8d-111">*...*</span><span class="sxs-lookup"><span data-stu-id="16e8d-111">*...*</span></span> 
<span data-ttu-id="16e8d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16e8d-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="16e8d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16e8d-113">Requirements</span></span>



| <span data-ttu-id="16e8d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e8d-114">Requirement</span></span> | <span data-ttu-id="16e8d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="16e8d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16e8d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="16e8d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="16e8d-117"><dt>Msmdun80.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16e8d-117"><dt>Msmdun80.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e8d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="16e8d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e8d-119">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="16e8d-119">**GetDiskFreeSpaceEx**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)
</dt> </dl>

 

 
