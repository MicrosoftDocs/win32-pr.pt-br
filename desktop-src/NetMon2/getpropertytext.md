---
description: A função GetPropertyText retorna um ponteiro para o texto da propriedade.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Função GetPropertyText (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296199"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="8c56e-103">Função GetPropertyText</span><span class="sxs-lookup"><span data-stu-id="8c56e-103">GetPropertyText function</span></span>

<span data-ttu-id="8c56e-104">A função **GetPropertyText** retorna um ponteiro para o texto da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c56e-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c56e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c56e-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="8c56e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c56e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c56e-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c56e-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c56e-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="8c56e-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="8c56e-109">*lpPI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c56e-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c56e-110">Ponteiro para uma instância de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c56e-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="8c56e-111">*szBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c56e-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c56e-112">Ponteiro para a cadeia de texto da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c56e-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="8c56e-113">*BufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c56e-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c56e-114">Tamanho do buffer de cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="8c56e-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c56e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c56e-115">Return value</span></span>

<span data-ttu-id="8c56e-116">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o texto da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c56e-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="8c56e-117">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8c56e-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c56e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c56e-118">Remarks</span></span>

<span data-ttu-id="8c56e-119">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetPropertyText** .</span><span class="sxs-lookup"><span data-stu-id="8c56e-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c56e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c56e-120">Requirements</span></span>



| <span data-ttu-id="8c56e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c56e-121">Requirement</span></span> | <span data-ttu-id="8c56e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8c56e-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c56e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c56e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c56e-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c56e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8c56e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c56e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c56e-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c56e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8c56e-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c56e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c56e-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c56e-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8c56e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c56e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c56e-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c56e-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c56e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8c56e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c56e-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c56e-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




