---
description: Fornece funcionalidade para geração de número aleatório, conversões e codificação e decodificação de Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Objeto Utilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754586"
---
# <a name="utilities-object"></a><span data-ttu-id="6fb7f-103">Objeto Utilities</span><span class="sxs-lookup"><span data-stu-id="6fb7f-103">Utilities object</span></span>

<span data-ttu-id="6fb7f-104">\[O objeto **Utilities** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="6fb7f-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="6fb7f-105">O objeto **Utilities** fornece funcionalidade para geração de número aleatório, conversões e codificação e decodificação de Base64.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="6fb7f-106">Quando usar</span><span class="sxs-lookup"><span data-stu-id="6fb7f-106">When to use</span></span>

<span data-ttu-id="6fb7f-107">O objeto **Utilities** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="6fb7f-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="6fb7f-108">Codifique uma cadeia de caracteres como Base64 ou decodifique uma cadeia de caracteres de Base64.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="6fb7f-109">Converter uma cadeia de caracteres de pacote binário em uma matriz de bytes e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="6fb7f-110">Converter uma cadeia de caracteres de um binário compactado em uma cadeia de caracteres hexadecimal e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="6fb7f-111">Gerar um número aleatório seguro.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="6fb7f-112">Converter a hora local em tempo universal coordenado (hora de Greenwich) e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="6fb7f-113">Membros</span><span class="sxs-lookup"><span data-stu-id="6fb7f-113">Members</span></span>

<span data-ttu-id="6fb7f-114">O objeto **Utilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6fb7f-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="6fb7f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fb7f-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6fb7f-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fb7f-116">Methods</span></span>

<span data-ttu-id="6fb7f-117">O objeto **Utilities** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="6fb7f-118">Método</span><span class="sxs-lookup"><span data-stu-id="6fb7f-118">Method</span></span>                                                               | <span data-ttu-id="6fb7f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fb7f-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="6fb7f-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="6fb7f-121">Decodifica uma cadeia de caracteres de Base64.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="6fb7f-122">**Base64Encode**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="6fb7f-123">Codifica uma cadeia de caracteres como Base64.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="6fb7f-124">**BinaryStringToByteArray**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="6fb7f-125">Converte uma cadeia de caracteres de pacote binário em uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="6fb7f-126">**BinaryToHex**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="6fb7f-127">Converte uma cadeia de caracteres de pacote binário em uma cadeia de caracteres hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="6fb7f-128">**ByteArrayToBinaryString**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="6fb7f-129">Converte uma matriz de bytes em uma cadeia de caracteres de pacote binário.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="6fb7f-130">**Getrandom**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="6fb7f-131">Gera um número aleatório seguro.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="6fb7f-132">**HexToBinary**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="6fb7f-133">Converte uma cadeia de caracteres hexadecimal em uma cadeia de caracteres de pacote binário.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="6fb7f-134">**LocalTimeToUTCTime**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="6fb7f-135">Converte a hora local do computador em tempo universal coordenado.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="6fb7f-136">**UTCTimeToLocalTime**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="6fb7f-137">Converte o tempo universal coordenado na hora local do computador.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6fb7f-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fb7f-138">Remarks</span></span>

<span data-ttu-id="6fb7f-139">O objeto **Utilities** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="6fb7f-140">O ProgID para o objeto **Utilities** é CAPICOM. Utilities. 1.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb7f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fb7f-141">Requirements</span></span>



| <span data-ttu-id="6fb7f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb7f-142">Requirement</span></span> | <span data-ttu-id="6fb7f-143">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb7f-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb7f-144">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6fb7f-144">Redistributable</span></span><br/> | <span data-ttu-id="6fb7f-145">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6fb7f-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6fb7f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb7f-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="6fb7f-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb7f-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




