---
description: Inicializa o compartilhamento do IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Função FInitIMEShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752925"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="808b5-103">Função FInitIMEShare</span><span class="sxs-lookup"><span data-stu-id="808b5-103">FInitIMEShare function</span></span>

<span data-ttu-id="808b5-104">Inicializa o compartilhamento do IME.</span><span class="sxs-lookup"><span data-stu-id="808b5-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="808b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="808b5-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="808b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="808b5-106">Parameters</span></span>

<span data-ttu-id="808b5-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="808b5-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="808b5-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="808b5-108">Return value</span></span>

<span data-ttu-id="808b5-109">Caso contrário, a função retornará **true** ou **false** .</span><span class="sxs-lookup"><span data-stu-id="808b5-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="808b5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="808b5-110">Remarks</span></span>

<span data-ttu-id="808b5-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="808b5-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="808b5-112">Essa função deve ser chamada antes de qualquer outra função de compartilhamento do IME ser chamada.</span><span class="sxs-lookup"><span data-stu-id="808b5-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="808b5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="808b5-113">Requirements</span></span>



| <span data-ttu-id="808b5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="808b5-114">Requirement</span></span> | <span data-ttu-id="808b5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="808b5-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="808b5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="808b5-116">DLL</span></span><br/> | <dl> <span data-ttu-id="808b5-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="808b5-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="808b5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="808b5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808b5-119">**EndIMEShare**</span><span class="sxs-lookup"><span data-stu-id="808b5-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 
