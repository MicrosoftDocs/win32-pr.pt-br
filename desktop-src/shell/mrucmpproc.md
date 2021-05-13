---
description: Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).
title: Função de retorno de chamada MRUCMPPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840777"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="5a378-103">Função de retorno de chamada MRUCMPPROC</span><span class="sxs-lookup"><span data-stu-id="5a378-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="5a378-104">Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="5a378-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a378-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a378-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="5a378-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a378-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="5a378-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a378-108">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="5a378-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="5a378-109">A primeira cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5a378-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="5a378-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="5a378-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a378-111">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="5a378-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="5a378-112">Uma segunda cadeia de caracteres para comparar com a primeira.</span><span class="sxs-lookup"><span data-stu-id="5a378-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a378-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a378-113">Return value</span></span>

<span data-ttu-id="5a378-114">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5a378-114">Type: **int**</span></span>

<span data-ttu-id="5a378-115">Retornará 0 se os itens forem idênticos, caso contrário, um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5a378-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a378-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a378-116">Remarks</span></span>

<span data-ttu-id="5a378-117">Essa função pode ser especificada opcionalmente para uso na estrutura [**MRUINFO**](mruinfo.md) passada para [**CreateMRUListW**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="5a378-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="5a378-118">Isso é útil quando a lista MRU foi criada com o **sinalizador \_ binário MRU** .</span><span class="sxs-lookup"><span data-stu-id="5a378-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="5a378-119">Quando essa função não é especificada, as funções de comparação de cadeia de caracteres padrão são usadas.</span><span class="sxs-lookup"><span data-stu-id="5a378-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a378-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a378-120">Requirements</span></span>



| <span data-ttu-id="5a378-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a378-121">Requirement</span></span> | <span data-ttu-id="5a378-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5a378-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5a378-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a378-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5a378-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a378-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="5a378-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a378-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5a378-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a378-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="5a378-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5a378-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5a378-128">**MRUCMPPROCW** (Unicode) e **MRUCMPPROCA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5a378-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




