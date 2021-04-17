---
description: Fecha um item de dados especificado do armazenamento protegido.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'Método IPStore:: CloseItem (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e5f550df0ffa4dd2f35a91e768d70bb0359b9a4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762865"
---
# <a name="ipstorecloseitem-method"></a><span data-ttu-id="6624e-103">Método IPStore:: CloseItem</span><span class="sxs-lookup"><span data-stu-id="6624e-103">IPStore::CloseItem method</span></span>

<span data-ttu-id="6624e-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6624e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6624e-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6624e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6624e-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="6624e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6624e-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6624e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6624e-108">Fecha um item de dados especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="6624e-108">Closes a specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="6624e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6624e-109">Syntax</span></span>


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6624e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6624e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6624e-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6624e-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6624e-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="6624e-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="6624e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6624e-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="6624e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6624e-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="6624e-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="6624e-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="6624e-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="6624e-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="6624e-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6624e-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6624e-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="6624e-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6624e-119">*pItemType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6624e-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6624e-120">Um ponteiro para um **GUID** que identifica o tipo de dados do item a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="6624e-120">A pointer to a **GUID** that identifies the data type of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="6624e-121">*pItemSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6624e-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6624e-122">Um ponteiro para um **GUID** que indica o subtipo de item a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="6624e-122">A pointer to a **GUID** that indicates the item subtype to close.</span></span>

</dd> <dt>

<span data-ttu-id="6624e-123">*szItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6624e-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6624e-124">Uma cadeia de caracteres que contém o nome do item a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="6624e-124">A string that contains the name of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="6624e-125">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6624e-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6624e-126">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6624e-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6624e-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6624e-127">Return value</span></span>

<span data-ttu-id="6624e-128">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6624e-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="6624e-129">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6624e-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6624e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6624e-130">Requirements</span></span>



| <span data-ttu-id="6624e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6624e-131">Requirement</span></span> | <span data-ttu-id="6624e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6624e-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6624e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6624e-133">Header</span></span><br/> | <dl> <span data-ttu-id="6624e-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6624e-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6624e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6624e-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="6624e-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6624e-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6624e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6624e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6624e-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6624e-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
