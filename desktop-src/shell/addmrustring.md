---
description: Adiciona uma cadeia de caracteres à parte superior da lista de MRU (usados mais recentemente).
title: Função AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841187"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="e4c09-103">Função AddMRUStringW</span><span class="sxs-lookup"><span data-stu-id="e4c09-103">AddMRUStringW function</span></span>

<span data-ttu-id="e4c09-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e4c09-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="e4c09-105">Ele pode ser alterado ou não disponível nas versões subsequentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c09-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="e4c09-106">\]</span><span class="sxs-lookup"><span data-stu-id="e4c09-106">\]</span></span>

<span data-ttu-id="e4c09-107">Adiciona uma cadeia de caracteres à parte superior da lista de MRU (usados mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="e4c09-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c09-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4c09-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="e4c09-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4c09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c09-110">*hMRU* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="e4c09-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c09-111">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="e4c09-111">Type: **HANDLE**</span></span>

<span data-ttu-id="e4c09-112">O alça da lista mru.</span><span class="sxs-lookup"><span data-stu-id="e4c09-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="e4c09-113">*szString* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="e4c09-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c09-114">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="e4c09-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="e4c09-115">Um ponteiro para os dados.</span><span class="sxs-lookup"><span data-stu-id="e4c09-115">A pointer to the data.</span></span> <span data-ttu-id="e4c09-116">Isso pode ser uma cadeia de caracteres ou, se a lista mru foi criada com o sinalizador **\_ BINARY do MRU,** dados binários.</span><span class="sxs-lookup"><span data-stu-id="e4c09-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="e4c09-117">No caso de dados binários, a primeira **DWORD** indica seu tamanho.</span><span class="sxs-lookup"><span data-stu-id="e4c09-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c09-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4c09-118">Return value</span></span>

<span data-ttu-id="e4c09-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="e4c09-119">Type: **int**</span></span>

<span data-ttu-id="e4c09-120">Retornará um valor não negativo se for bem-sucedido; caso contrário, -1.</span><span class="sxs-lookup"><span data-stu-id="e4c09-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4c09-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4c09-121">Remarks</span></span>

<span data-ttu-id="e4c09-122">Essa função não está incluída em um header ou biblioteca público.</span><span class="sxs-lookup"><span data-stu-id="e4c09-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="e4c09-123">Ele pode ser acessado por [**meio de GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído do comctl32.dll por seu ordinal, que é 401 para **AddMRUStringW.**</span><span class="sxs-lookup"><span data-stu-id="e4c09-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c09-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4c09-124">Requirements</span></span>



| <span data-ttu-id="e4c09-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c09-125">Requirement</span></span> | <span data-ttu-id="e4c09-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e4c09-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c09-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4c09-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c09-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4c09-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4c09-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4c09-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c09-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4c09-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4c09-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c09-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c09-132"><dt>Comctl32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e4c09-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="e4c09-133">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e4c09-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e4c09-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="e4c09-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

