---
description: A função LoadStringAddr transforma uma cadeia de caracteres (como &\# 0034; 157.54.32.45&\# 0034;) e cria um endereço DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Função LoadStringAddr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770142"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="b7cef-103">Função LoadStringAddr</span><span class="sxs-lookup"><span data-stu-id="b7cef-103">LoadStringAddr function</span></span>

<span data-ttu-id="b7cef-104">A função **LoadStringAddr** transforma uma cadeia de caracteres (como "157.54.32.45") e cria um endereço **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b7cef-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7cef-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="b7cef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7cef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7cef-107">*pAddress*</span><span class="sxs-lookup"><span data-stu-id="b7cef-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="b7cef-108">Ponteiro para um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b7cef-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="b7cef-109">*str*</span><span class="sxs-lookup"><span data-stu-id="b7cef-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="b7cef-110">Ponteiro para uma cadeia de caracteres com a representação x. x. x de um endereço IP (por exemplo, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="b7cef-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7cef-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7cef-111">Return value</span></span>

<span data-ttu-id="b7cef-112">Se a função for bem-sucedida (o nome do endereço foi encontrado); o valor de retorno é **true**.</span><span class="sxs-lookup"><span data-stu-id="b7cef-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="b7cef-113">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="b7cef-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7cef-114">Requirements</span></span>



| <span data-ttu-id="b7cef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7cef-115">Requirement</span></span> | <span data-ttu-id="b7cef-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b7cef-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cef-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7cef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7cef-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b7cef-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b7cef-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7cef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7cef-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b7cef-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b7cef-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b7cef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7cef-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7cef-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b7cef-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7cef-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7cef-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7cef-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b7cef-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7cef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7cef-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7cef-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




