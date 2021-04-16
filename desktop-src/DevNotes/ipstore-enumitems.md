---
description: Retorna o ponteiro de interface de um subtipo para enumerar itens no banco de dados de armazenamento protegido.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Método IPStore:: EnumItems (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747485"
---
# <a name="ipstoreenumitems-method"></a><span data-ttu-id="ec700-103">Método IPStore:: EnumItems</span><span class="sxs-lookup"><span data-stu-id="ec700-103">IPStore::EnumItems method</span></span>

<span data-ttu-id="ec700-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ec700-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ec700-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ec700-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ec700-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="ec700-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ec700-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ec700-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ec700-108">Retorna o ponteiro de interface de um subtipo para enumerar itens no banco de dados de armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="ec700-108">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec700-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec700-109">Syntax</span></span>


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="ec700-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec700-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec700-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec700-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec700-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="ec700-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="ec700-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ec700-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="ec700-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ec700-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="ec700-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="ec700-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="ec700-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="ec700-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="ec700-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ec700-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ec700-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="ec700-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ec700-119">*pItemType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec700-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec700-120">Um ponteiro para um **GUID** que identifica o tipo de dados do item a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="ec700-120">A pointer to a **GUID** that identifies the data type of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="ec700-121">*pItemSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec700-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec700-122">Um ponteiro para um **GUID** que identifica o subtipo de dados do item a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="ec700-122">A pointer to a **GUID** that identifies the data subtype of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="ec700-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec700-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec700-124">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="ec700-124">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec700-125">*ppEnum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec700-125">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec700-126">Um ponteiro para um ponteiro para uma interface [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="ec700-126">A pointer to a pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec700-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec700-127">Return value</span></span>

<span data-ttu-id="ec700-128">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ec700-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="ec700-129">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ec700-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec700-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec700-130">Requirements</span></span>



| <span data-ttu-id="ec700-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec700-131">Requirement</span></span> | <span data-ttu-id="ec700-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ec700-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec700-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec700-133">Header</span></span><br/> | <dl> <span data-ttu-id="ec700-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec700-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ec700-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ec700-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="ec700-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec700-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec700-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec700-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec700-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="ec700-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
