---
description: Traduz a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Função RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089071"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="ac420-103">Função RtlUnicodeToUTF8N</span><span class="sxs-lookup"><span data-stu-id="ac420-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="ac420-104">Traduz a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="ac420-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac420-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac420-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="ac420-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac420-107">*UTF8StringDestination* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac420-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac420-108">Um ponteiro para um buffer alocado pelo chamador para receber a cadeia de caracteres traduzida.</span><span class="sxs-lookup"><span data-stu-id="ac420-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="ac420-109">*UTF8StringMaxByteCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac420-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac420-110">Número máximo de bytes a serem gravados em *UTF8StringDestination*.</span><span class="sxs-lookup"><span data-stu-id="ac420-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="ac420-111">Se esse valor fizer com que a cadeia de caracteres traduzida seja truncada, **RtlUnicodeToUTF8N** retornará um status de erro.</span><span class="sxs-lookup"><span data-stu-id="ac420-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="ac420-112">*UTF8StringActualByteCount* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac420-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac420-113">Um ponteiro para uma variável alocada pelo chamador que recebe o comprimento, em bytes, da cadeia de caracteres traduzida.</span><span class="sxs-lookup"><span data-stu-id="ac420-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="ac420-114">Esse parâmetro é opcional e pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ac420-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="ac420-115">Se a cadeia de caracteres for truncada, o número retornado contará a contagem de cadeia de caracteres truncada real.</span><span class="sxs-lookup"><span data-stu-id="ac420-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="ac420-116">*UnicodeStringSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac420-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac420-117">Um ponteiro para a cadeia de caracteres de origem Unicode a ser traduzido.</span><span class="sxs-lookup"><span data-stu-id="ac420-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="ac420-118">\* UnicodeStringByteCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac420-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac420-119">Especifica o número de bytes na cadeia de caracteres de origem Unicode ao qual o parâmetro *UnicodeStringSource* aponta.</span><span class="sxs-lookup"><span data-stu-id="ac420-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac420-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac420-120">Return value</span></span>

<span data-ttu-id="ac420-121">**RtlUnicodeToUTF8N** retorna um dos seguintes valores de NTSTATUS:</span><span class="sxs-lookup"><span data-stu-id="ac420-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="ac420-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ac420-122">Return code</span></span>                                                                                                  | <span data-ttu-id="ac420-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac420-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac420-124"><dt>**STATUS com \_ êxito**</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="ac420-125">A cadeia de caracteres Unicode foi convertida em UTF-8.</span><span class="sxs-lookup"><span data-stu-id="ac420-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ac420-126"><dt>**STATUS \_ alguns \_ não \_ mapeados**</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="ac420-127">Um caractere de entrada inválido foi encontrado e substituído.</span><span class="sxs-lookup"><span data-stu-id="ac420-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="ac420-128">Esse status é considerado um status de êxito.</span><span class="sxs-lookup"><span data-stu-id="ac420-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="ac420-129"><dt>**parâmetro de STATUS \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="ac420-130">Ambos os ponteiros para *UTF8StringDestination* e *UTF8StringActualByteCount* eram **nulos**.</span><span class="sxs-lookup"><span data-stu-id="ac420-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="ac420-131"><dt>**\_Parâmetro inválido \_ \_ 4 do status**</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="ac420-132">O *UnicodeStringSource* era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ac420-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="ac420-133"><dt>**BUFFER de STATUS \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="ac420-134">*UTF8StringDestination* foi truncado.</span><span class="sxs-lookup"><span data-stu-id="ac420-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="ac420-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac420-135">Remarks</span></span>

<span data-ttu-id="ac420-136">Embora *UTF8StringActualByteCount* seja opcional e possa ser **NULL**, os chamadores devem fornecer armazenamento para ele, pois o comprimento recebido pode ser usado para determinar se a conversão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ac420-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="ac420-137">Essa rotina não modifica a cadeia de caracteres de origem.</span><span class="sxs-lookup"><span data-stu-id="ac420-137">This routine does not modify the source string.</span></span> <span data-ttu-id="ac420-138">Ele retornará uma cadeia de caracteres UTF-8 terminada em nulo se o *UnicodeStringSource* fornecido incluísse um terminador nulo e se o *UTF8StringMaxByteCount* especificado não causar truncamento.</span><span class="sxs-lookup"><span data-stu-id="ac420-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="ac420-139">Se a saída estiver truncada e um caractere de entrada inválido for encontrado, a função retornará um erro de buffer de STATUS \_ \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="ac420-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="ac420-140">Se *UTF8StringDestination* for definido como **NULL** , a função retornará o número necessário de bytes para hospedar a cadeia de caracteres traduzida sem qualquer truncamento em *UTF8StringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="ac420-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="ac420-141">Os chamadores de **RtlUnicodeToUTF8N** devem estar em execução em IRQL < nível de expedição \_ .</span><span class="sxs-lookup"><span data-stu-id="ac420-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac420-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac420-142">Requirements</span></span>



| <span data-ttu-id="ac420-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac420-143">Requirement</span></span> | <span data-ttu-id="ac420-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ac420-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac420-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac420-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ac420-146">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ac420-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ac420-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac420-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ac420-148">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ac420-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac420-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac420-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac420-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="ac420-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ac420-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac420-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac420-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac420-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac420-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac420-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="ac420-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 




