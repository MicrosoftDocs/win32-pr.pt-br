---
description: Inicializa o rastreamento.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: Função InitAsyncTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747487"
---
# <a name="initasynctrace-function"></a><span data-ttu-id="ee207-103">Função InitAsyncTrace</span><span class="sxs-lookup"><span data-stu-id="ee207-103">InitAsyncTrace function</span></span>

<span data-ttu-id="ee207-104">Inicializa o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ee207-104">Initializes the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee207-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee207-105">Syntax</span></span>


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="ee207-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee207-106">Parameters</span></span>

<span data-ttu-id="ee207-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ee207-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee207-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ee207-108">Return value</span></span>

<span data-ttu-id="ee207-109">Essa função retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ee207-109">This function returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee207-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee207-110">Remarks</span></span>

<span data-ttu-id="ee207-111">Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="ee207-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="ee207-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ee207-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee207-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee207-113">Requirements</span></span>



| <span data-ttu-id="ee207-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee207-114">Requirement</span></span> | <span data-ttu-id="ee207-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ee207-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee207-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ee207-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ee207-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee207-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
