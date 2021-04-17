---
description: A função GetFrameDstAddressOffset retorna o deslocamento para o endereço de destino de um determinado quadro.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Função GetFrameDstAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775675"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="37e0c-103">Função GetFrameDstAddressOffset</span><span class="sxs-lookup"><span data-stu-id="37e0c-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="37e0c-104">A função **GetFrameDstAddressOffset** retorna o deslocamento para o endereço de destino de um determinado quadro.</span><span class="sxs-lookup"><span data-stu-id="37e0c-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e0c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37e0c-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="37e0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37e0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37e0c-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37e0c-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37e0c-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="37e0c-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="37e0c-109">*AddressType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37e0c-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37e0c-110">Tipo do endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="37e0c-110">Type of the destination address.</span></span> <span data-ttu-id="37e0c-111">Especifique um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="37e0c-111">Specify one of the following values:</span></span>

<span data-ttu-id="37e0c-112">tipo de endereço endereço Ethernet tipo de endereço IP tipo de endereço \_ \_ \_ \_ \_ \_ IPX \_ tipo de \_ endereço TOKENRING \_ tipo \_ \_ \_ \_ \_ \_ \_ \_ do endereço FDDI tipo de endereço do XNS tipo de endereços IP tipo de endereço ATM.</span><span class="sxs-lookup"><span data-stu-id="37e0c-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="37e0c-113">*AddressLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37e0c-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37e0c-114">Comprimento do endereço de destino, em bytes.</span><span class="sxs-lookup"><span data-stu-id="37e0c-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37e0c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37e0c-115">Return value</span></span>

<span data-ttu-id="37e0c-116">Se a função for bem-sucedida, o valor de retorno será o deslocamento (medido em bytes) para o tipo de endereço solicitado.</span><span class="sxs-lookup"><span data-stu-id="37e0c-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="37e0c-117">Se a função não for bem-sucedida, o valor de retorno será menos um (-1).</span><span class="sxs-lookup"><span data-stu-id="37e0c-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="37e0c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="37e0c-118">Remarks</span></span>

<span data-ttu-id="37e0c-119">Se o parâmetro *AddressType* for definido como tipo de endereço \_ \_ Ethernet, o valor de retorno da função **GetFrameDstAddressOffset** será sempre zero.</span><span class="sxs-lookup"><span data-stu-id="37e0c-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="37e0c-120">O deslocamento de um endereço Ethernet é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="37e0c-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="37e0c-121">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameDstAddressOffset** .</span><span class="sxs-lookup"><span data-stu-id="37e0c-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e0c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37e0c-122">Requirements</span></span>



| <span data-ttu-id="37e0c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="37e0c-123">Requirement</span></span> | <span data-ttu-id="37e0c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="37e0c-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="37e0c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37e0c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37e0c-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="37e0c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="37e0c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37e0c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37e0c-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="37e0c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="37e0c-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="37e0c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="37e0c-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="37e0c-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="37e0c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37e0c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="37e0c-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37e0c-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="37e0c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="37e0c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37e0c-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37e0c-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




