---
description: Obtém informações sobre a versão do sistema operacional.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: Função _GetVersionEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752929"
---
# <a name="_getversionex-function"></a><span data-ttu-id="0fcec-103">\_Função GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="0fcec-103">\_GetVersionEx function</span></span>

<span data-ttu-id="0fcec-104">\[Essa função é um wrapper sobre a função **GetVersionEx** .</span><span class="sxs-lookup"><span data-stu-id="0fcec-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="0fcec-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="0fcec-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="0fcec-106">Os aplicativos devem chamar **GetVersionEx** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="0fcec-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="0fcec-107">Obtém informações sobre a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0fcec-107">Gets information about the operating system version.</span></span> <span data-ttu-id="0fcec-108">Consulte [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span><span class="sxs-lookup"><span data-stu-id="0fcec-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fcec-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="0fcec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fcec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcec-111">*...*</span><span class="sxs-lookup"><span data-stu-id="0fcec-111">*...*</span></span> 
<span data-ttu-id="0fcec-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0fcec-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0fcec-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fcec-113">Requirements</span></span>



| <span data-ttu-id="0fcec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fcec-114">Requirement</span></span> | <span data-ttu-id="0fcec-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0fcec-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcec-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0fcec-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0fcec-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fcec-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fcec-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fcec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcec-119">**GetVersionEx**</span><span class="sxs-lookup"><span data-stu-id="0fcec-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
