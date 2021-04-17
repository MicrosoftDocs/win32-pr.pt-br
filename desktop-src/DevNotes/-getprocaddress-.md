---
description: Obtém o endereço de uma função de uma DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: Função _GetProcAddress_
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755813"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="df2cc-103">\_\_Função GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="df2cc-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="df2cc-104">\[Essa função é um wrapper sobre a função **GetProcAddress** .</span><span class="sxs-lookup"><span data-stu-id="df2cc-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="df2cc-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="df2cc-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="df2cc-106">Os aplicativos devem chamar o **GetProcAddress** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="df2cc-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="df2cc-107">Obtém o endereço de uma função de uma DLL.</span><span class="sxs-lookup"><span data-stu-id="df2cc-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="df2cc-108">Consulte [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="df2cc-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="df2cc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df2cc-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="df2cc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df2cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df2cc-111">*...*</span><span class="sxs-lookup"><span data-stu-id="df2cc-111">*...*</span></span> 
<span data-ttu-id="df2cc-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="df2cc-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="df2cc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df2cc-113">Requirements</span></span>



| <span data-ttu-id="df2cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="df2cc-114">Requirement</span></span> | <span data-ttu-id="df2cc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="df2cc-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df2cc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="df2cc-116">DLL</span></span><br/> | <dl> <span data-ttu-id="df2cc-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df2cc-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df2cc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="df2cc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df2cc-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="df2cc-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
