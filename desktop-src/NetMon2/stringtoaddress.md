---
description: A função StringToAddress converte uma cadeia de caracteres em um endereço.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Função StringToAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760042"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="d45d5-103">Função StringToAddress</span><span class="sxs-lookup"><span data-stu-id="d45d5-103">StringToAddress function</span></span>

<span data-ttu-id="d45d5-104">A função **StringToAddress** converte uma cadeia de caracteres em um endereço.</span><span class="sxs-lookup"><span data-stu-id="d45d5-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d45d5-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="d45d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d45d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d45d5-107">*lpAddress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d45d5-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d45d5-108">Ponteiro para o endereço para o qual a cadeia de caracteres é convertida.</span><span class="sxs-lookup"><span data-stu-id="d45d5-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="d45d5-109">*cadeia de caracteres* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d45d5-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d45d5-110">Cadeia de caracteres que é convertida em um endereço.</span><span class="sxs-lookup"><span data-stu-id="d45d5-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d45d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d45d5-111">Return value</span></span>

<span data-ttu-id="d45d5-112">O valor de retorno é um ponteiro para a cadeia de caracteres convertida.</span><span class="sxs-lookup"><span data-stu-id="d45d5-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="d45d5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d45d5-113">Requirements</span></span>



| <span data-ttu-id="d45d5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d45d5-114">Requirement</span></span> | <span data-ttu-id="d45d5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d45d5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d45d5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d45d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d45d5-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d45d5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d45d5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d45d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d45d5-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d45d5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d45d5-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d45d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d45d5-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d45d5-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d45d5-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d45d5-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d45d5-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d45d5-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="d45d5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d45d5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d45d5-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d45d5-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




