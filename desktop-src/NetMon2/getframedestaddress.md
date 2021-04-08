---
description: Recupera o endereço de destino de um quadro.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Função GetFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920702"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="e24fe-103">Função GetFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="e24fe-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="e24fe-104">A função **GetFrameDestAddress** recupera o endereço de destino de um quadro.</span><span class="sxs-lookup"><span data-stu-id="e24fe-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e24fe-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e24fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e24fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24fe-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="e24fe-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="e24fe-108">Um identificador do quadro para o qual obter um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e24fe-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="e24fe-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="e24fe-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="e24fe-110">Um buffer de retorno que armazena o endereço de destino do quadro.</span><span class="sxs-lookup"><span data-stu-id="e24fe-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e24fe-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="e24fe-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="e24fe-112">Um tipo de endereço, como tipo de \_ endereço \_ Ethernet ou tipo de endereço \_ \_ IP.</span><span class="sxs-lookup"><span data-stu-id="e24fe-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="e24fe-113">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="e24fe-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e24fe-114">Os sinalizadores usados para modificar os dados de endereço de destino retornados.</span><span class="sxs-lookup"><span data-stu-id="e24fe-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="e24fe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e24fe-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="e24fe-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e24fe-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="e24fe-117"><dt>**sinalizadores de ADDRESStype \_ \_ NORMALIZE**</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="e24fe-118">Cancela os BITs de grupo e de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e24fe-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="e24fe-119"><dt>**sinalizadores de \_ \_ bits \_ invertidos de endereço**</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="e24fe-120">Converte endereços de rede de token ring de volta em normal.</span><span class="sxs-lookup"><span data-stu-id="e24fe-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24fe-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e24fe-121">Return value</span></span>

<span data-ttu-id="e24fe-122">Se a função for bem-sucedida, o valor de *lpAddress* será válido e o valor de retorno será BHERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e24fe-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="e24fe-123">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e24fe-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="e24fe-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e24fe-124">Return code</span></span>                                                                                                | <span data-ttu-id="e24fe-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="e24fe-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e24fe-126"><dt>**\_protocolo BHERR \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="e24fe-127">O protocolo especificado no parâmetro *AddressType* é inválido para o quadro.</span><span class="sxs-lookup"><span data-stu-id="e24fe-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="e24fe-128"><dt>**BHERR \_ HFRAME inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="e24fe-129">O valor de *hFrame* é inválido.</span><span class="sxs-lookup"><span data-stu-id="e24fe-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="e24fe-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e24fe-130">Remarks</span></span>

<span data-ttu-id="e24fe-131">O tipo de endereço localizar tipo de endereço **\_ \_ \_ mais alto** é permitido.</span><span class="sxs-lookup"><span data-stu-id="e24fe-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="e24fe-132">Quando esse tipo de endereço é usado, a função procura o endereço IP IPX, XNS, IP ou VINEs antes de retornar o endereço ETHERNET, TOKENRING ou FDDI.</span><span class="sxs-lookup"><span data-stu-id="e24fe-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="e24fe-133">Essa abordagem é útil para protocolos e em ambientes em que duas NICs podem ser multiplexada em um único endereço de servidor.</span><span class="sxs-lookup"><span data-stu-id="e24fe-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24fe-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e24fe-134">Requirements</span></span>



| <span data-ttu-id="e24fe-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24fe-135">Requirement</span></span> | <span data-ttu-id="e24fe-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e24fe-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e24fe-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e24fe-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e24fe-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e24fe-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e24fe-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e24fe-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e24fe-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e24fe-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e24fe-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e24fe-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24fe-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e24fe-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e24fe-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="e24fe-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e24fe-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e24fe-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e24fe-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e24fe-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




