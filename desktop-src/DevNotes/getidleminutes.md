---
description: Obtém o período de tempo, em minutos, desde a última atividade do usuário.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Função GetIdleMinutes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750134"
---
# <a name="getidleminutes-function"></a><span data-ttu-id="fcb81-103">Função GetIdleMinutes</span><span class="sxs-lookup"><span data-stu-id="fcb81-103">GetIdleMinutes function</span></span>

<span data-ttu-id="fcb81-104">\[Essa função não tem suporte e pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="fcb81-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="fcb81-105">Em vez disso, use a função **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="fcb81-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="fcb81-106">Obtém o período de tempo, em minutos, desde a última atividade do usuário.</span><span class="sxs-lookup"><span data-stu-id="fcb81-106">Gets the length of time, in minutes, since the user's last activity.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb81-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcb81-107">Syntax</span></span>


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="fcb81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcb81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb81-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="fcb81-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb81-110">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="fcb81-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcb81-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcb81-111">Return value</span></span>

<span data-ttu-id="fcb81-112">Retorna o número de minutos desde a última atividade do usuário.</span><span class="sxs-lookup"><span data-stu-id="fcb81-112">Returns the number of minutes since the user's last activity.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb81-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcb81-113">Remarks</span></span>

<span data-ttu-id="fcb81-114">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fcb81-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="fcb81-115">Esta função não é exportada pelo nome; Especifique o ordinal 8 ao chamar **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="fcb81-115">This function is not exported by name; specify ordinal 8 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb81-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcb81-116">Requirements</span></span>



| <span data-ttu-id="fcb81-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb81-117">Requirement</span></span> | <span data-ttu-id="fcb81-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fcb81-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb81-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fcb81-119">DLL</span></span><br/> | <dl> <span data-ttu-id="fcb81-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcb81-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb81-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcb81-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb81-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="fcb81-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
