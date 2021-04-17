---
description: Recupera o endereço de origem de um quadro.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Função GetFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770469"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="58d20-103">Função GetFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="58d20-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="58d20-104">A função **GetFrameSourceAddress** recupera o endereço de origem de um quadro.</span><span class="sxs-lookup"><span data-stu-id="58d20-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58d20-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="58d20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d20-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="58d20-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="58d20-108">Um identificador para o quadro para o qual um ponteiro deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="58d20-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="58d20-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="58d20-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="58d20-110">Um buffer de retorno que armazena o endereço de origem do quadro.</span><span class="sxs-lookup"><span data-stu-id="58d20-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="58d20-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="58d20-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="58d20-112">O tipo de endereço procurado, como tipo de endereço \_ \_ Ethernet ou tipo de \_ endereço \_ IP.</span><span class="sxs-lookup"><span data-stu-id="58d20-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="58d20-113">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="58d20-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="58d20-114">Os sinalizadores usados para modificar os dados de endereço de origem retornados.</span><span class="sxs-lookup"><span data-stu-id="58d20-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="58d20-115">Valor</span><span class="sxs-lookup"><span data-stu-id="58d20-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="58d20-116">Significado</span><span class="sxs-lookup"><span data-stu-id="58d20-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="58d20-117"><dt>**sinalizadores de ADDRESStype \_ \_ NORMALIZE**</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="58d20-118">Cancela os BITs de grupo e de roteamento.</span><span class="sxs-lookup"><span data-stu-id="58d20-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="58d20-119"><dt>**sinalizadores de \_ \_ bits \_ invertidos de endereço**</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="58d20-120">Converte endereços de rede de token ring de volta em normal.</span><span class="sxs-lookup"><span data-stu-id="58d20-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58d20-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58d20-121">Return value</span></span>

<span data-ttu-id="58d20-122">Se a função for bem-sucedida, o valor de *lpAddress* será válido e o valor de retorno será BHERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="58d20-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="58d20-123">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="58d20-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="58d20-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="58d20-124">Return code</span></span>                                                                                                | <span data-ttu-id="58d20-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="58d20-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58d20-126"><dt>**\_protocolo BHERR \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="58d20-127">O protocolo especificado pelo parâmetro *AddressType* é inválido para o quadro.</span><span class="sxs-lookup"><span data-stu-id="58d20-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="58d20-128"><dt>**BHERR \_ HFRAME inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="58d20-129">O valor do parâmetro *hFrame* é inválido.</span><span class="sxs-lookup"><span data-stu-id="58d20-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="58d20-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="58d20-130">Remarks</span></span>

<span data-ttu-id="58d20-131">É permitido um tipo de endereço de **tipo de endereço \_ \_ \_ mais alto** .</span><span class="sxs-lookup"><span data-stu-id="58d20-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="58d20-132">Quando esse tipo de endereço é usado, a função procura o endereço IP IPX, XNS, IP ou VINEs antes de retornar o endereço ETHERNET, TOKENRING ou FDDI.</span><span class="sxs-lookup"><span data-stu-id="58d20-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="58d20-133">Essa abordagem é útil para protocolos e ambientes nos quais duas NICs podem ser multiplexada em um único endereço de servidor.</span><span class="sxs-lookup"><span data-stu-id="58d20-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d20-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58d20-134">Requirements</span></span>



| <span data-ttu-id="58d20-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="58d20-135">Requirement</span></span> | <span data-ttu-id="58d20-136">Valor</span><span class="sxs-lookup"><span data-stu-id="58d20-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="58d20-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58d20-137">Minimum supported client</span></span><br/> | <span data-ttu-id="58d20-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58d20-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="58d20-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58d20-139">Minimum supported server</span></span><br/> | <span data-ttu-id="58d20-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58d20-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="58d20-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="58d20-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="58d20-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="58d20-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58d20-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="58d20-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="58d20-145">DLL</span><span class="sxs-lookup"><span data-stu-id="58d20-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58d20-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58d20-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




