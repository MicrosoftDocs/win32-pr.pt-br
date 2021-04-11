---
description: Traduz a cadeia de caracteres de origem especificada em uma cadeia de caracteres Unicode, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Função RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163976"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="9fe53-103">Função RtlUTF8ToUnicodeN</span><span class="sxs-lookup"><span data-stu-id="9fe53-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="9fe53-104">Traduz a cadeia de caracteres de origem especificada em uma cadeia de caracteres Unicode, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="9fe53-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fe53-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="9fe53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fe53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fe53-107">*UnicodeStringDestination* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe53-108">Um ponteiro para um buffer alocado pelo chamador que recebe a cadeia de caracteres traduzida.</span><span class="sxs-lookup"><span data-stu-id="9fe53-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="9fe53-109">*UnicodeStringMaxByteCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe53-110">Número máximo de bytes a serem gravados em *UnicodeStringDestination*.</span><span class="sxs-lookup"><span data-stu-id="9fe53-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="9fe53-111">Se esse valor fizer com que a cadeia de caracteres traduzida seja truncada, **RtlUTF8ToUnicodeN** retornará um status de erro.</span><span class="sxs-lookup"><span data-stu-id="9fe53-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="9fe53-112">*UnicodeStringActualByteCount* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe53-113">Um ponteiro para uma variável alocada pelo chamador que recebe o comprimento, em bytes, da cadeia de caracteres traduzida.</span><span class="sxs-lookup"><span data-stu-id="9fe53-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="9fe53-114">Esse parâmetro é opcional e pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9fe53-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="9fe53-115">Se a cadeia de caracteres for truncada, o número retornado contará a contagem de cadeia de caracteres truncada real.</span><span class="sxs-lookup"><span data-stu-id="9fe53-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="9fe53-116">*UTF8StringSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe53-117">Um ponteiro para a cadeia de caracteres a ser traduzida.</span><span class="sxs-lookup"><span data-stu-id="9fe53-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="9fe53-118">*UTF8StringByteCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe53-119">Tamanho, em bytes, da cadeia de caracteres em *UTF8StringSource*.</span><span class="sxs-lookup"><span data-stu-id="9fe53-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fe53-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fe53-120">Return value</span></span>

<span data-ttu-id="9fe53-121">**RtlUTF8ToUnicodeN** retorna um dos seguintes valores de NTSTATUS:</span><span class="sxs-lookup"><span data-stu-id="9fe53-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="9fe53-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9fe53-122">Return code</span></span>                                                                                                  | <span data-ttu-id="9fe53-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fe53-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9fe53-124"><dt>**STATUS com \_ êxito**</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="9fe53-125">A cadeia de caracteres foi convertida em Unicode.</span><span class="sxs-lookup"><span data-stu-id="9fe53-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="9fe53-126"><dt>**STATUS \_ alguns \_ não \_ mapeados**</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="9fe53-127">Um caractere de entrada inválido foi encontrado e substituído.</span><span class="sxs-lookup"><span data-stu-id="9fe53-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="9fe53-128">Esse status é considerado um status de êxito.</span><span class="sxs-lookup"><span data-stu-id="9fe53-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="9fe53-129"><dt>**parâmetro de STATUS \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="9fe53-130">Ambos os ponteiros para *UnicodeStringDestination* e *UnicodeStringActualByteCount* eram **nulos**.</span><span class="sxs-lookup"><span data-stu-id="9fe53-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="9fe53-131"><dt>**\_Parâmetro inválido \_ \_ 4 do status**</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="9fe53-132">O *UTF8StringSource* era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9fe53-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="9fe53-133"><dt>**BUFFER de STATUS \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="9fe53-134">*UnicodeStringDestination* foi truncado.</span><span class="sxs-lookup"><span data-stu-id="9fe53-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="9fe53-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fe53-135">Remarks</span></span>

<span data-ttu-id="9fe53-136">Embora *UnicodeStringActualByteCount* seja opcional e possa ser **NULL**, os chamadores devem fornecer armazenamento para ele, pois o comprimento recebido pode ser usado para determinar se a conversão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9fe53-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="9fe53-137">Se a saída estiver truncada e um caractere de entrada inválido for encontrado, a função retornará um erro de buffer de STATUS \_ \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="9fe53-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="9fe53-138">Se *UnicodeStringDestination* for definido como **NULL** , a função retornará o número necessário de bytes para hospedar a cadeia de caracteres traduzida sem qualquer truncamento em *UnicodeStringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="9fe53-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="9fe53-139">**RtlUTF8ToUnicodeN** não modifica a cadeia de caracteres de origem, a menos que os ponteiros *UnicodeStringDestination* e *UTF8StringSource* sejam equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9fe53-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="9fe53-140">A cadeia de caracteres Unicode retornada não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="9fe53-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="9fe53-141">Os chamadores de **RtlUTF8ToUnicodeN** devem estar em execução em IRQL < nível de expedição \_ .</span><span class="sxs-lookup"><span data-stu-id="9fe53-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe53-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fe53-142">Requirements</span></span>



| <span data-ttu-id="9fe53-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe53-143">Requirement</span></span> | <span data-ttu-id="9fe53-144">Valor</span><span class="sxs-lookup"><span data-stu-id="9fe53-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe53-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fe53-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe53-146">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9fe53-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fe53-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe53-148">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="9fe53-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9fe53-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fe53-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fe53-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="9fe53-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe53-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe53-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe53-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe53-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fe53-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe53-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="9fe53-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




