---
description: A função GetPropertyInfo retorna um ponteiro para as informações de propriedade de um determinado protocolo.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Função GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826833"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="336d5-103">Função GetPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="336d5-103">GetPropertyInfo function</span></span>

<span data-ttu-id="336d5-104">A função **GetPropertyInfo** retorna um ponteiro para as informações de propriedade de um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="336d5-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="336d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="336d5-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="336d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="336d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="336d5-107">*hProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="336d5-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="336d5-108">Identificador para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="336d5-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="336d5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="336d5-109">Return value</span></span>

<span data-ttu-id="336d5-110">Se a função for bem-sucedida, o valor de retorno será um ponteiro para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="336d5-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="336d5-111">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="336d5-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="336d5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="336d5-112">Remarks</span></span>

<span data-ttu-id="336d5-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetPropertyInfo** .</span><span class="sxs-lookup"><span data-stu-id="336d5-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="336d5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="336d5-114">Requirements</span></span>



| <span data-ttu-id="336d5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="336d5-115">Requirement</span></span> | <span data-ttu-id="336d5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="336d5-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="336d5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="336d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="336d5-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="336d5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="336d5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="336d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="336d5-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="336d5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="336d5-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="336d5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="336d5-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="336d5-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="336d5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="336d5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="336d5-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="336d5-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="336d5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="336d5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="336d5-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="336d5-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




