---
description: Encerra o monitoramento de inatividade.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Função EndIdleDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751353"
---
# <a name="endidledetection-function"></a><span data-ttu-id="bbdeb-103">Função EndIdleDetection</span><span class="sxs-lookup"><span data-stu-id="bbdeb-103">EndIdleDetection function</span></span>

<span data-ttu-id="bbdeb-104">\[Essa função não tem suporte e pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="bbdeb-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bbdeb-105">Em vez disso, use a função **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="bbdeb-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="bbdeb-106">Encerra o monitoramento de inatividade.</span><span class="sxs-lookup"><span data-stu-id="bbdeb-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbdeb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbdeb-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="bbdeb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbdeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbdeb-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="bbdeb-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="bbdeb-110">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="bbdeb-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbdeb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbdeb-111">Return value</span></span>

<span data-ttu-id="bbdeb-112">Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="bbdeb-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbdeb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbdeb-113">Remarks</span></span>

<span data-ttu-id="bbdeb-114">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="bbdeb-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="bbdeb-115">Esta função não é exportada pelo nome; Especifique o ordinal 4 ao chamar **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="bbdeb-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbdeb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbdeb-116">Requirements</span></span>



| <span data-ttu-id="bbdeb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbdeb-117">Requirement</span></span> | <span data-ttu-id="bbdeb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bbdeb-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdeb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bbdeb-119">DLL</span></span><br/> | <dl> <span data-ttu-id="bbdeb-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbdeb-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbdeb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbdeb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbdeb-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="bbdeb-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
