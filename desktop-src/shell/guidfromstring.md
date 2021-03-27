---
description: Converte uma cadeia de caracteres em um GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Função GUIDFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828299"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="0792f-103">Função GUIDFromString</span><span class="sxs-lookup"><span data-stu-id="0792f-103">GUIDFromString function</span></span>

<span data-ttu-id="0792f-104">\[O **GUIDFromString** está disponível por meio do Windows XP com Service Pack 2 (SP2) ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0792f-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="0792f-105">Ele pode ser alterado ou indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0792f-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0792f-106">Os aplicativos devem usar [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) ou [**falha em IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) no lugar dessa função.\]</span><span class="sxs-lookup"><span data-stu-id="0792f-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="0792f-107">Converte uma cadeia de caracteres em um GUID.</span><span class="sxs-lookup"><span data-stu-id="0792f-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0792f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0792f-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="0792f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0792f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0792f-110">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0792f-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0792f-111">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="0792f-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="0792f-112">Um ponteiro para a cadeia de caracteres terminada em nulo a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="0792f-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="0792f-113">A cadeia de caracteres deve estar no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="0792f-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="0792f-114">*pGuid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0792f-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0792f-115">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="0792f-115">Type: **LPGUID**</span></span>

<span data-ttu-id="0792f-116">Ponteiro para um buffer para receber o GUID quando esse método retorna.</span><span class="sxs-lookup"><span data-stu-id="0792f-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0792f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0792f-117">Return value</span></span>

<span data-ttu-id="0792f-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0792f-118">Type: **BOOL**</span></span>

<span data-ttu-id="0792f-119">**True** se o GUID foi criado com êxito; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="0792f-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0792f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0792f-120">Remarks</span></span>

<span data-ttu-id="0792f-121">Essa função não é declarada em um cabeçalho ou exportada pelo nome de um arquivo. dll.</span><span class="sxs-lookup"><span data-stu-id="0792f-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="0792f-122">Ele deve ser carregado de Shell32.dll como ordinal 703 para **GUIDFromStringA** e ordinal 704 para **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="0792f-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="0792f-123">Ele também pode ser acessado de Shlwapi.dll como ordinal 269 para **GUIDFromStringA** e ordinal 270 para **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="0792f-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0792f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0792f-124">Requirements</span></span>



| <span data-ttu-id="0792f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0792f-125">Requirement</span></span> | <span data-ttu-id="0792f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0792f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0792f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0792f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0792f-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0792f-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0792f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0792f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0792f-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0792f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0792f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0792f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0792f-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0792f-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="0792f-133">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0792f-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0792f-134">**GUIDFromStringW** (Unicode) e **GUIDFromStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0792f-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
