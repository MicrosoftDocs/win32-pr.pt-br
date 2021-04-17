---
description: Cria o subtipo especificado dentro do tipo especificado.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Método IPStore:: CreateSubtype (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751553"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="c206d-103">Método IPStore:: CreateSubtype</span><span class="sxs-lookup"><span data-stu-id="c206d-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="c206d-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c206d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c206d-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c206d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c206d-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="c206d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c206d-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="c206d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c206d-108">Cria o subtipo especificado dentro do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="c206d-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c206d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c206d-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c206d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c206d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c206d-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c206d-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c206d-112">Especifica a área de armazenamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="c206d-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="c206d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c206d-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="c206d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c206d-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="c206d-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="c206d-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="c206d-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="c206d-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="c206d-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c206d-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c206d-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="c206d-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c206d-119">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c206d-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c206d-120">Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c206d-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="c206d-121">*pSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c206d-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c206d-122">Um ponteiro para um **GUID** que identifica o subtipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c206d-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="c206d-123">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c206d-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c206d-124">Um ponteiro para uma estrutura de [**\_ TYPEINFO de PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c206d-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c206d-125">*pRules* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c206d-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c206d-126">Um ponteiro para uma [**estrutura \_ ACCESSRULESET de PST**](pst-accessruleset.md) .</span><span class="sxs-lookup"><span data-stu-id="c206d-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="c206d-127">**Windows XP:** Esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c206d-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c206d-128">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c206d-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c206d-129">Reservado deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="c206d-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c206d-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c206d-130">Return value</span></span>

<span data-ttu-id="c206d-131">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c206d-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="c206d-132">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c206d-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c206d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c206d-133">Requirements</span></span>



| <span data-ttu-id="c206d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c206d-134">Requirement</span></span> | <span data-ttu-id="c206d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c206d-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c206d-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c206d-136">Header</span></span><br/> | <dl> <span data-ttu-id="c206d-137"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="c206d-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c206d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c206d-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="c206d-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c206d-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c206d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c206d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c206d-141">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="c206d-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="c206d-142">**\_ACCESSRULESET PST**</span><span class="sxs-lookup"><span data-stu-id="c206d-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="c206d-143">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="c206d-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
