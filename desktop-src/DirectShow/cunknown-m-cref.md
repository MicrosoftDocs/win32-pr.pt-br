---
description: 'CUnknown:: m_cRef contagem de referência de membro.'
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'Membro CUnknown:: m_cRef (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084574"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="5b092-103">Membro cRef CUnknown:: m \_</span><span class="sxs-lookup"><span data-stu-id="5b092-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="5b092-104">Contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="5b092-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b092-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b092-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="5b092-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b092-106">Remarks</span></span>

<span data-ttu-id="5b092-107">Use essa variável de membro se você substituir o método [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) ou [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="5b092-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b092-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b092-108">Requirements</span></span>



| <span data-ttu-id="5b092-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b092-109">Requirement</span></span> | <span data-ttu-id="5b092-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5b092-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b092-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b092-111">Header</span></span><br/>  | <dl> <span data-ttu-id="5b092-112"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b092-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b092-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b092-113">Library</span></span><br/> | <dl> <span data-ttu-id="5b092-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5b092-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




