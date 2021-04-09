---
description: Usa chamadas sequenciais para recuperar todas as cadeias de caracteres dentro dos intervalos especificados.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Função GetStringsFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920688"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="acb11-103">Função GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="acb11-104">A função **GetStringsFromBlob** usa chamadas sequenciais para recuperar todas as cadeias de caracteres dentro dos intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="acb11-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="acb11-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acb11-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="acb11-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acb11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb11-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="acb11-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-108">Um identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="acb11-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-109">*pRequestedOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="acb11-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-110">Um ponteiro para a seção de proprietário da qual obter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="acb11-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-111">*pRequestedCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="acb11-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-112">Um ponteiro para a seção de categoria da qual obter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="acb11-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-113">*pRequestedTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="acb11-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-114">Um ponteiro para a marca da cadeia de caracteres solicitada.</span><span class="sxs-lookup"><span data-stu-id="acb11-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-115">*ppReturnedOwnerName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="acb11-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-116">Um ponteiro para a variável que aponta para onde o nome do **proprietário** será retornado.</span><span class="sxs-lookup"><span data-stu-id="acb11-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-117">*ppReturnedCategoryName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="acb11-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-118">Um ponteiro para a variável que aponta para onde o nome da **categoria** será retornado.</span><span class="sxs-lookup"><span data-stu-id="acb11-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-119">*ppReturnedTagName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="acb11-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-120">Um ponteiro para a variável que aponta para onde o nome da **marca** será retornado.</span><span class="sxs-lookup"><span data-stu-id="acb11-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-121">*ppReturnedString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="acb11-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-122">Um ponteiro para a variável que aponta para onde o nome da cadeia de caracteres será retornado.</span><span class="sxs-lookup"><span data-stu-id="acb11-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="acb11-123">*pRestartKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="acb11-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb11-124">Um ponteiro para a variável em que a chave de reinicialização será especificada e retornada.</span><span class="sxs-lookup"><span data-stu-id="acb11-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb11-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acb11-125">Return value</span></span>

<span data-ttu-id="acb11-126">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="acb11-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="acb11-127">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o problema.</span><span class="sxs-lookup"><span data-stu-id="acb11-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="acb11-128">Se uma combinação especificada de informações de **proprietário**, **categoria** e **marca** não existir, o valor de retorno será **a \_ entrada de blob NMERR não \_ \_ \_ \_ existir**.</span><span class="sxs-lookup"><span data-stu-id="acb11-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="acb11-129">Quando o BLOB é atravessado completamente dentro dos limites especificados inicialmente, a função retorna a **\_ entrada de blob NMERR \_ \_ \_ não \_ existe** e o parâmetro *pRestartKey* aponta para zero.</span><span class="sxs-lookup"><span data-stu-id="acb11-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb11-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="acb11-130">Remarks</span></span>

<span data-ttu-id="acb11-131">Na chamada inicial para a função **GetStringsFromBlob** , o parâmetro *pRestartKey* aponta para uma variável que contém o valor zero.</span><span class="sxs-lookup"><span data-stu-id="acb11-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="acb11-132">Os parâmetros de *busca* podem ser usados somente quando a chave de reinicialização for zero.</span><span class="sxs-lookup"><span data-stu-id="acb11-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="acb11-133">Em chamadas subsequentes, quando *pRestartKey* tem valores diferentes de zero, os parâmetros de *busca* são ignorados.</span><span class="sxs-lookup"><span data-stu-id="acb11-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="acb11-134">Na chamada inicial, tudo pode apontar para **NULL**, que configura a consulta para retornar cada entrada no BLOB, uma por chamada subsequente.</span><span class="sxs-lookup"><span data-stu-id="acb11-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="acb11-135">A especificação de um proprietário limita as cadeias de caracteres retornadas apenas ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="acb11-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="acb11-136">Uma limitação semelhante é verdadeira para categorias e marcas, com a limitação adicional de que, se uma categoria for especificada, um proprietário também deverá ser especificado e, se uma marca for especificada, uma categoria (e, portanto, um proprietário) deverá ser especificada.</span><span class="sxs-lookup"><span data-stu-id="acb11-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="acb11-137">Quando a chamada inicial para **GetStringsFromBlob** retorna, *pRestartKey* aponta para um novo valor, que deve ser especificado na próxima chamada para a função para obter o próximo valor.</span><span class="sxs-lookup"><span data-stu-id="acb11-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb11-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acb11-138">Requirements</span></span>



| <span data-ttu-id="acb11-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="acb11-139">Requirement</span></span> | <span data-ttu-id="acb11-140">Valor</span><span class="sxs-lookup"><span data-stu-id="acb11-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acb11-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb11-141">Minimum supported client</span></span><br/> | <span data-ttu-id="acb11-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acb11-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="acb11-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb11-143">Minimum supported server</span></span><br/> | <span data-ttu-id="acb11-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acb11-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acb11-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="acb11-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb11-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb11-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="acb11-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acb11-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="acb11-148"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acb11-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="acb11-149">DLL</span><span class="sxs-lookup"><span data-stu-id="acb11-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acb11-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acb11-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb11-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="acb11-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb11-152">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-153">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-154">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-155">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-156">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-157">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-158">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-159">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-160">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="acb11-161">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="acb11-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 




