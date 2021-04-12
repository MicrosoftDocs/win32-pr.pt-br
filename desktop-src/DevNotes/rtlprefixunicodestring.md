---
description: Compara duas cadeias de caracteres Unicode para determinar se uma cadeia é um prefixo da outra.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Função RtlPrefixUnicodeString (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456978"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="00c6e-103">Função RtlPrefixUnicodeString</span><span class="sxs-lookup"><span data-stu-id="00c6e-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="00c6e-104">Compara duas cadeias de caracteres Unicode para determinar se uma cadeia é um prefixo da outra.</span><span class="sxs-lookup"><span data-stu-id="00c6e-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c6e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00c6e-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="00c6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c6e-107">*Seqüência1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00c6e-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c6e-108">Ponteiro para a primeira cadeia de caracteres, que pode ser um prefixo da cadeia de caracteres Unicode em buffer em *seqüência2*.</span><span class="sxs-lookup"><span data-stu-id="00c6e-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="00c6e-109">*Seqüência2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00c6e-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c6e-110">Ponteiro para a segunda cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="00c6e-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="00c6e-111">*CaseInSensitive* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00c6e-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c6e-112">Se **for true**, o caso deverá ser ignorado ao fazer a comparação.</span><span class="sxs-lookup"><span data-stu-id="00c6e-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c6e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00c6e-113">Return value</span></span>

<span data-ttu-id="00c6e-114">**True** se *seqüência1* for um prefixo de *seqüência2*.</span><span class="sxs-lookup"><span data-stu-id="00c6e-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c6e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00c6e-115">Requirements</span></span>



| <span data-ttu-id="00c6e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00c6e-116">Requirement</span></span> | <span data-ttu-id="00c6e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="00c6e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c6e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00c6e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00c6e-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="00c6e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="00c6e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00c6e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00c6e-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="00c6e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="00c6e-122">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="00c6e-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="00c6e-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="00c6e-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="00c6e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00c6e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="00c6e-125"><dt>Ntddk. h (incluir Ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00c6e-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="00c6e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00c6e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="00c6e-127"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00c6e-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="00c6e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="00c6e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c6e-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c6e-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="00c6e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="00c6e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c6e-131">**RtlCompareUnicodeString**</span><span class="sxs-lookup"><span data-stu-id="00c6e-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




