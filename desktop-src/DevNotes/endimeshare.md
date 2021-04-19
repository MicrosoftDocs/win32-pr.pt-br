---
description: Encerra o compartilhamento do IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: Função EndIMEShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755406"
---
# <a name="endimeshare-function"></a><span data-ttu-id="a3d03-103">Função EndIMEShare</span><span class="sxs-lookup"><span data-stu-id="a3d03-103">EndIMEShare function</span></span>

<span data-ttu-id="a3d03-104">Encerra o compartilhamento do IME.</span><span class="sxs-lookup"><span data-stu-id="a3d03-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d03-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="a3d03-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d03-106">Parameters</span></span>

<span data-ttu-id="a3d03-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a3d03-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3d03-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3d03-108">Return value</span></span>

<span data-ttu-id="a3d03-109">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a3d03-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d03-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3d03-110">Remarks</span></span>

<span data-ttu-id="a3d03-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a3d03-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="a3d03-112">Essa função deve ser chamada após a última função de compartilhamento do IME ser chamada.</span><span class="sxs-lookup"><span data-stu-id="a3d03-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d03-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3d03-113">Requirements</span></span>



| <span data-ttu-id="a3d03-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d03-114">Requirement</span></span> | <span data-ttu-id="a3d03-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a3d03-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d03-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a3d03-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a3d03-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3d03-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d03-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3d03-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d03-119">**FInitIMEShare**</span><span class="sxs-lookup"><span data-stu-id="a3d03-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 
