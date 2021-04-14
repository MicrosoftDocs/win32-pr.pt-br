---
title: Método ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: O método ISoftKbd ShowKeysForKeyScanMode exibe as chaves usadas para o modo de verificação de chave para um teclado virtual.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Estrutura de serviços de texto do método ShowKeysForKeyScanMode
- Método ShowKeysForKeyScanMode de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455642"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="9eb11-106">Método ISoftKbd:: ShowKeysForKeyScanMode</span><span class="sxs-lookup"><span data-stu-id="9eb11-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="9eb11-107">O método **ISoftKbd:: ShowKeysForKeyScanMode** exibe as chaves usadas para o modo de verificação de chave para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb11-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb11-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eb11-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="9eb11-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb11-110">*lpKeyID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eb11-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb11-111">Ponteiro para uma matriz de elementos KEYID que indica os identificadores de chaves a serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="9eb11-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="9eb11-112">*iKeyNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eb11-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb11-113">O número de chaves a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="9eb11-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="9eb11-114">*fHighL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eb11-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb11-115">TRUE se o método for realçar as chaves; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="9eb11-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb11-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eb11-116">Return value</span></span>

<span data-ttu-id="9eb11-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9eb11-117">This method can return one of these values.</span></span>



| <span data-ttu-id="9eb11-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9eb11-118">Value</span></span>                                                                                        | <span data-ttu-id="9eb11-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9eb11-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9eb11-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9eb11-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9eb11-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9eb11-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="9eb11-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9eb11-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9eb11-123">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="9eb11-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9eb11-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb11-124">Requirements</span></span>



| <span data-ttu-id="9eb11-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb11-125">Requirement</span></span> | <span data-ttu-id="9eb11-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9eb11-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb11-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eb11-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb11-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9eb11-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9eb11-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eb11-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb11-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9eb11-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9eb11-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9eb11-131">Redistributable</span></span><br/>          | <span data-ttu-id="9eb11-132">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9eb11-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="9eb11-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9eb11-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb11-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb11-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="9eb11-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="9eb11-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9eb11-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9eb11-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="9eb11-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb11-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb11-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb11-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb11-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eb11-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb11-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="9eb11-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





