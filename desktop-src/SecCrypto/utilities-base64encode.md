---
description: Codifica uma cadeia de caracteres como Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Método Utilities. Base64Encode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800072"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="177d3-103">Método Utilities. Base64Encode</span><span class="sxs-lookup"><span data-stu-id="177d3-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="177d3-104">\[O método **Base64Encode** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="177d3-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="177d3-105">O método **Base64Encode** codifica uma cadeia de caracteres como Base64.</span><span class="sxs-lookup"><span data-stu-id="177d3-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="177d3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="177d3-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="177d3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="177d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="177d3-108">*SrcString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="177d3-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="177d3-109">A cadeia de caracteres para codificar como Base64.</span><span class="sxs-lookup"><span data-stu-id="177d3-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="177d3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="177d3-110">Return value</span></span>

<span data-ttu-id="177d3-111">A cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="177d3-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="177d3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="177d3-112">Remarks</span></span>

<span data-ttu-id="177d3-113">A codificação Base64 é o esquema usado para transmitir dados binários.</span><span class="sxs-lookup"><span data-stu-id="177d3-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="177d3-114">A base64 processa dados como grupos de 24 bits, mapeando esses dados para quatro caracteres codificados.</span><span class="sxs-lookup"><span data-stu-id="177d3-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="177d3-115">A codificação Base64 é, às vezes, chamada de codificação 3 para 4.</span><span class="sxs-lookup"><span data-stu-id="177d3-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="177d3-116">Cada 6 bits do grupo de 24 bits é usado como um índice em uma tabela de mapeamento (o alfabeto Base64) para obter um caractere para os dados codificados.</span><span class="sxs-lookup"><span data-stu-id="177d3-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="177d3-117">Os dados codificados têm comprimentos de linha limitados a 76 caracteres.</span><span class="sxs-lookup"><span data-stu-id="177d3-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="177d3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="177d3-118">Requirements</span></span>



| <span data-ttu-id="177d3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="177d3-119">Requirement</span></span> | <span data-ttu-id="177d3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="177d3-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="177d3-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="177d3-121">Redistributable</span></span><br/> | <span data-ttu-id="177d3-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="177d3-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="177d3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="177d3-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="177d3-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="177d3-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177d3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="177d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177d3-126">**Utilitários**</span><span class="sxs-lookup"><span data-stu-id="177d3-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




