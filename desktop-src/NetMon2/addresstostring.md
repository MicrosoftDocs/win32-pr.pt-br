---
description: A função AddressToString converte um endereço em uma cadeia de caracteres.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Função AddressToString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091794"
---
# <a name="addresstostring-function"></a><span data-ttu-id="27110-103">Função AddressToString</span><span class="sxs-lookup"><span data-stu-id="27110-103">AddressToString function</span></span>

<span data-ttu-id="27110-104">A função **AddressToString** converte um endereço em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="27110-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="27110-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27110-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="27110-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27110-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27110-107">*cadeia de caracteres* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27110-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27110-108">Cadeia de caracteres para a qual o endereço é convertido.</span><span class="sxs-lookup"><span data-stu-id="27110-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="27110-109">*lpAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27110-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27110-110">O endereço que é impresso.</span><span class="sxs-lookup"><span data-stu-id="27110-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27110-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27110-111">Return value</span></span>

<span data-ttu-id="27110-112">O valor de retorno é um ponteiro para a cadeia de caracteres convertida.</span><span class="sxs-lookup"><span data-stu-id="27110-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="27110-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27110-113">Requirements</span></span>



| <span data-ttu-id="27110-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="27110-114">Requirement</span></span> | <span data-ttu-id="27110-115">Valor</span><span class="sxs-lookup"><span data-stu-id="27110-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27110-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27110-116">Minimum supported client</span></span><br/> | <span data-ttu-id="27110-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="27110-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="27110-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27110-118">Minimum supported server</span></span><br/> | <span data-ttu-id="27110-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="27110-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27110-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="27110-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="27110-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27110-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="27110-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27110-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="27110-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27110-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="27110-124">DLL</span><span class="sxs-lookup"><span data-stu-id="27110-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27110-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27110-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




