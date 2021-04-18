---
description: Obtém o nome do computador.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: Função _GetComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749060"
---
# <a name="_getcomputername-function"></a><span data-ttu-id="6abd5-103">\_Função GetComputerName</span><span class="sxs-lookup"><span data-stu-id="6abd5-103">\_GetComputerName function</span></span>

<span data-ttu-id="6abd5-104">\[Essa função é um wrapper sobre a função **GetComputerName** .</span><span class="sxs-lookup"><span data-stu-id="6abd5-104">\[This function is a wrapper over the **GetComputerName** function.</span></span> <span data-ttu-id="6abd5-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="6abd5-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="6abd5-106">Os aplicativos devem chamar **Getcomputernamename** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="6abd5-106">Applications should call **GetComputerName** directly.\]</span></span>

<span data-ttu-id="6abd5-107">Obtém o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="6abd5-107">Gets the computer name.</span></span> <span data-ttu-id="6abd5-108">Consulte [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span><span class="sxs-lookup"><span data-stu-id="6abd5-108">See [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="6abd5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6abd5-109">Syntax</span></span>


```C++
BOOL _GetComputerName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="6abd5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6abd5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abd5-111">*...*</span><span class="sxs-lookup"><span data-stu-id="6abd5-111">*...*</span></span> 
<span data-ttu-id="6abd5-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6abd5-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6abd5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6abd5-113">Requirements</span></span>



| <span data-ttu-id="6abd5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6abd5-114">Requirement</span></span> | <span data-ttu-id="6abd5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6abd5-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6abd5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6abd5-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6abd5-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6abd5-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abd5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6abd5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abd5-119">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="6abd5-119">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
