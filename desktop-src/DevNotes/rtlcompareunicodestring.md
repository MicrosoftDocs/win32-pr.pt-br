---
description: Compara duas cadeias de caracteres Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Função RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826358"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="f6c3d-103">Função RtlCompareUnicodeString</span><span class="sxs-lookup"><span data-stu-id="f6c3d-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="f6c3d-104">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c3d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6c3d-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="f6c3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6c3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c3d-107">*Seqüência1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6c3d-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c3d-108">Ponteiro para a primeira cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="f6c3d-109">*Seqüência2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6c3d-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c3d-110">Ponteiro para a segunda cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="f6c3d-111">*CaseInSensitive* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6c3d-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c3d-112">Se **for true**, o caso deverá ser ignorado ao fazer a comparação.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c3d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6c3d-113">Return value</span></span>

<span data-ttu-id="f6c3d-114">Um valor assinado que fornece os resultados da comparação:</span><span class="sxs-lookup"><span data-stu-id="f6c3d-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="f6c3d-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f6c3d-115">Return code</span></span>                                                                               | <span data-ttu-id="f6c3d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6c3d-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f6c3d-117"><dt>**Zero**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="f6c3d-118">*Seqüência1* é igual a *seqüência2*.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="f6c3d-119"><dt>**< zero**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="f6c3d-120">*Seqüência1* é menor que *seqüência2*.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="f6c3d-121"><dt>**> zero**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="f6c3d-122">*Seqüência1* é maior que *seqüência2*.</span><span class="sxs-lookup"><span data-stu-id="f6c3d-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f6c3d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6c3d-123">Requirements</span></span>



| <span data-ttu-id="f6c3d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c3d-124">Requirement</span></span> | <span data-ttu-id="f6c3d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f6c3d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c3d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c3d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c3d-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6c3d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="f6c3d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c3d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c3d-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6c3d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="f6c3d-130">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="f6c3d-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="f6c3d-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="f6c3d-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6c3d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c3d-133"><dt>WDM. h (incluindo WDM. h, Ntddk. h ou Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="f6c3d-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6c3d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6c3d-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f6c3d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c3d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6c3d-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6c3d-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="f6c3d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6c3d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c3d-139">**RtlCompareString**</span><span class="sxs-lookup"><span data-stu-id="f6c3d-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="f6c3d-140">**RtlEqualString**</span><span class="sxs-lookup"><span data-stu-id="f6c3d-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
