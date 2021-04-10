---
description: A função GetFrameSrcAddressOffset retorna o deslocamento do endereço de origem dos quadros.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Função GetFrameSrcAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170661"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="6e4e5-103">Função GetFrameSrcAddressOffset</span><span class="sxs-lookup"><span data-stu-id="6e4e5-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="6e4e5-104">A função **GetFrameSrcAddressOffset** retorna o deslocamento do endereço de origem do quadro.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e4e5-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="6e4e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e4e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e4e5-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="6e4e5-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4e5-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e5-109">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="6e4e5-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4e5-110">Tipo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-110">Source address type.</span></span> <span data-ttu-id="6e4e5-111">O valor do parâmetro pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6e4e5-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="6e4e5-112">tipo de endereço \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="6e4e5-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="6e4e5-113">\_IP do tipo de endereço \_</span><span class="sxs-lookup"><span data-stu-id="6e4e5-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="6e4e5-114">tipo de endereço \_ \_ IPX</span><span class="sxs-lookup"><span data-stu-id="6e4e5-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="6e4e5-115">tipo de endereço \_ \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="6e4e5-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="6e4e5-116">tipo de endereço \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="6e4e5-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="6e4e5-117">tipo de endereço \_ \_ XNS</span><span class="sxs-lookup"><span data-stu-id="6e4e5-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="6e4e5-118">\_IP de \_ Vines de tipo de endereço \_</span><span class="sxs-lookup"><span data-stu-id="6e4e5-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="6e4e5-119">tipo de endereço \_ \_ ATM</span><span class="sxs-lookup"><span data-stu-id="6e4e5-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="6e4e5-120">*AddressLength*</span><span class="sxs-lookup"><span data-stu-id="6e4e5-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4e5-121">Ponteiro para uma **DWORD**, que, em retorno, contém o comprimento do endereço, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e4e5-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e4e5-122">Return value</span></span>

<span data-ttu-id="6e4e5-123">Se a função for bem-sucedida, o valor de retorno será o deslocamento para o endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="6e4e5-124">Se a função não for bem-sucedida, o valor de retorno será menos um (-1).</span><span class="sxs-lookup"><span data-stu-id="6e4e5-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e4e5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e4e5-125">Requirements</span></span>



| <span data-ttu-id="6e4e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e4e5-126">Requirement</span></span> | <span data-ttu-id="6e4e5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6e4e5-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4e5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e4e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6e4e5-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e4e5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6e4e5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e4e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6e4e5-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e4e5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e4e5-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e4e5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e4e5-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e4e5-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6e4e5-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e4e5-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e4e5-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e4e5-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e4e5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6e4e5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e4e5-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e4e5-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




