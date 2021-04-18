---
description: Move um arquivo ou diretório existente, incluindo seus filhos.
ms.assetid: 1c533b02-6674-4390-bc49-6420403778a8
title: Função _MoveFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MoveFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 44c57d562feff62e21c4c769bfc9d6a650f4984c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756012"
---
# <a name="_movefile-function"></a><span data-ttu-id="6b12e-103">\_Função MoveFile</span><span class="sxs-lookup"><span data-stu-id="6b12e-103">\_MoveFile function</span></span>

<span data-ttu-id="6b12e-104">\[Essa função é um wrapper sobre a função **MoveFile** .</span><span class="sxs-lookup"><span data-stu-id="6b12e-104">\[This function is a wrapper over the **MoveFile** function.</span></span> <span data-ttu-id="6b12e-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="6b12e-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="6b12e-106">Os aplicativos devem chamar **MoveFile** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="6b12e-106">Applications should call **MoveFile** directly.\]</span></span>

<span data-ttu-id="6b12e-107">Move um arquivo ou diretório existente, incluindo seus filhos.</span><span class="sxs-lookup"><span data-stu-id="6b12e-107">Moves an existing file or directory, including its children.</span></span> <span data-ttu-id="6b12e-108">Consulte [ **MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span><span class="sxs-lookup"><span data-stu-id="6b12e-108">See [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b12e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b12e-109">Syntax</span></span>


```C++
BOOL _MoveFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="6b12e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b12e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b12e-111">*...*</span><span class="sxs-lookup"><span data-stu-id="6b12e-111">*...*</span></span> 
<span data-ttu-id="6b12e-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6b12e-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6b12e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b12e-113">Requirements</span></span>



| <span data-ttu-id="6b12e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b12e-114">Requirement</span></span> | <span data-ttu-id="6b12e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6b12e-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b12e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6b12e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6b12e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b12e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b12e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b12e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b12e-119">**MoveFile**</span><span class="sxs-lookup"><span data-stu-id="6b12e-119">**MoveFile**</span></span>](/windows/win32/api/winbase/nf-winbase-movefile)
</dt> </dl>

 

 
