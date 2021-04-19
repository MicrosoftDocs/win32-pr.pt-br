---
description: Encerra o rastreamento.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: Função TermAsyncTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747290"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="88006-103">Função TermAsyncTrace</span><span class="sxs-lookup"><span data-stu-id="88006-103">TermAsyncTrace function</span></span>

<span data-ttu-id="88006-104">Encerra o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="88006-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="88006-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88006-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="88006-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88006-106">Parameters</span></span>

<span data-ttu-id="88006-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="88006-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88006-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="88006-108">Return value</span></span>

<span data-ttu-id="88006-109">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="88006-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88006-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="88006-110">Remarks</span></span>

<span data-ttu-id="88006-111">Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="88006-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="88006-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="88006-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="88006-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88006-113">Requirements</span></span>



| <span data-ttu-id="88006-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88006-114">Requirement</span></span> | <span data-ttu-id="88006-115">Valor</span><span class="sxs-lookup"><span data-stu-id="88006-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88006-116">DLL</span><span class="sxs-lookup"><span data-stu-id="88006-116">DLL</span></span><br/> | <dl> <span data-ttu-id="88006-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88006-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
