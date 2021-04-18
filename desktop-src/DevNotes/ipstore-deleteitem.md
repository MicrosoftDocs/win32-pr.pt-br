---
description: Exclui o item especificado do armazenamento protegido.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: 'IPStore: método eleteItem de:D (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749508"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="72d1d-103">IPStore: método eleteItem de:D</span><span class="sxs-lookup"><span data-stu-id="72d1d-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="72d1d-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72d1d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="72d1d-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="72d1d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="72d1d-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="72d1d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="72d1d-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="72d1d-108">Exclui o item especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="72d1d-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d1d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72d1d-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="72d1d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72d1d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d1d-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d1d-112">A área de armazenamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="72d1d-112">The provider storage area.</span></span>



| <span data-ttu-id="72d1d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="72d1d-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="72d1d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="72d1d-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="72d1d-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="72d1d-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="72d1d-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="72d1d-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="72d1d-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="72d1d-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="72d1d-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="72d1d-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72d1d-119">*pItemType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d1d-120">Um ponteiro para um **GUID** que identifica o tipo de dados do item a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="72d1d-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="72d1d-121">*pItemSubType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d1d-122">Um **GUID** que indica o subtipo de item a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="72d1d-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="72d1d-123">*szItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d1d-124">Uma cadeia de caracteres que contém o nome do item a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="72d1d-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="72d1d-125">*pPromptInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d1d-126">Um ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="72d1d-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="72d1d-127">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72d1d-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d1d-128">Especifica a interface do usuário e os comportamentos de segurança para a operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="72d1d-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="72d1d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="72d1d-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="72d1d-130">Significado</span><span class="sxs-lookup"><span data-stu-id="72d1d-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="72d1d-131"><dt>**PST \_ NENHUMA \_ \_ migração de interface do usuário**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="72d1d-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="72d1d-132">Não mostrar interface do usuário, a menos que uma senha personalizada seja necessária.</span><span class="sxs-lookup"><span data-stu-id="72d1d-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d1d-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72d1d-133">Return value</span></span>

<span data-ttu-id="72d1d-134">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72d1d-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="72d1d-135">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="72d1d-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d1d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72d1d-136">Requirements</span></span>



| <span data-ttu-id="72d1d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d1d-137">Requirement</span></span> | <span data-ttu-id="72d1d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="72d1d-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72d1d-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72d1d-139">Header</span></span><br/> | <dl> <span data-ttu-id="72d1d-140"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d1d-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="72d1d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="72d1d-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="72d1d-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d1d-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d1d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="72d1d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d1d-144">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="72d1d-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="72d1d-145">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="72d1d-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
