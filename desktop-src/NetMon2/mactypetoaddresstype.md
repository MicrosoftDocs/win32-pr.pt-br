---
description: A função MacTypeToAddressType converte um determinado tipo de MAC em um tipo de endereço.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Função MacTypeToAddressType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827259"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="790b1-103">Função MacTypeToAddressType</span><span class="sxs-lookup"><span data-stu-id="790b1-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="790b1-104">A função **MacTypeToAddressType** converte um determinado tipo de Mac em um tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="790b1-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="790b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="790b1-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="790b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="790b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790b1-107">*MacType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="790b1-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790b1-108">Tipo de MAC a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="790b1-108">MAC type to be converted.</span></span> <span data-ttu-id="790b1-109">Especifique um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="790b1-109">Specify one of the following values:</span></span>

<span data-ttu-id="790b1-110">MAC \_ tipo \_ Ethernet Mac \_ tipo \_ TOKENRING Mac \_ tipo \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="790b1-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790b1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="790b1-111">Return value</span></span>

<span data-ttu-id="790b1-112">Se a função for bem-sucedida, o valor de retorno será um dos seguintes tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="790b1-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="790b1-113">tipo de endereço \_ \_ Ethernet tipo de endereço \_ \_ TOKENRING tipo de endereço \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="790b1-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="790b1-114">Se a função não for bem-sucedida, o tipo de MAC será desconhecido, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="790b1-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="790b1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="790b1-115">Remarks</span></span>

<span data-ttu-id="790b1-116">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **MacTypeToAddressType** .</span><span class="sxs-lookup"><span data-stu-id="790b1-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="790b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="790b1-117">Requirements</span></span>



| <span data-ttu-id="790b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="790b1-118">Requirement</span></span> | <span data-ttu-id="790b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="790b1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="790b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="790b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="790b1-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="790b1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="790b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="790b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="790b1-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="790b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="790b1-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="790b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="790b1-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="790b1-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="790b1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="790b1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="790b1-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="790b1-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="790b1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="790b1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="790b1-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="790b1-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




