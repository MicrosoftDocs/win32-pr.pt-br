---
description: Grava um item de dados no armazenamento protegido.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Método IPStore:: WriteItem (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752597"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="2641a-103">Método IPStore:: WriteItem</span><span class="sxs-lookup"><span data-stu-id="2641a-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="2641a-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2641a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2641a-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2641a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2641a-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="2641a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2641a-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="2641a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2641a-108">Grava um item de dados no armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="2641a-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="2641a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2641a-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2641a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2641a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2641a-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-112">A área de armazenamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="2641a-112">The provider storage area.</span></span>



| <span data-ttu-id="2641a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2641a-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="2641a-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2641a-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="2641a-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="2641a-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="2641a-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="2641a-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2641a-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="2641a-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2641a-119">*pItemType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-120">Um ponteiro para um **GUID** que identifica o tipo de dados do item de dados que está sendo gravado.</span><span class="sxs-lookup"><span data-stu-id="2641a-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="2641a-121">*pItemSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-122">Um ponteiro para um **GUID** que identifica o subtipo de dados do item de dados que está sendo gravado.</span><span class="sxs-lookup"><span data-stu-id="2641a-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="2641a-123">*szItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-124">Um ponteiro para uma cadeia de caracteres que contém o nome atribuído ao item de dados armazenado.</span><span class="sxs-lookup"><span data-stu-id="2641a-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="2641a-125">*cbData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2641a-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-126">Um ponteiro para um **DWORD** que indica o tamanho do buffer que contém o item de dados armazenado.</span><span class="sxs-lookup"><span data-stu-id="2641a-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="2641a-127">*ppbData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2641a-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-128">Um ponteiro para um buffer que contém o item de dados que está sendo gravado.</span><span class="sxs-lookup"><span data-stu-id="2641a-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="2641a-129">*pProomptInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-130">Ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2641a-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2641a-131">*dwDefaultConfirmationStyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-132">O estilo de confirmação padrão.</span><span class="sxs-lookup"><span data-stu-id="2641a-132">The default confirmation style.</span></span>



| <span data-ttu-id="2641a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="2641a-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="2641a-134">Significado</span><span class="sxs-lookup"><span data-stu-id="2641a-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="2641a-135"><dt>**PST \_ \_Padrão de CF**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="2641a-136">Permite que o usuário escolha o estilo de confirmação.</span><span class="sxs-lookup"><span data-stu-id="2641a-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="2641a-137"><dt>**PST \_ CF \_ nenhum**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="2641a-138">Força a criação de itens silenciosos.</span><span class="sxs-lookup"><span data-stu-id="2641a-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="2641a-139">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2641a-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2641a-140">A interface do usuário e os comportamentos de segurança para a operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="2641a-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="2641a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="2641a-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="2641a-142">Significado</span><span class="sxs-lookup"><span data-stu-id="2641a-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="2641a-143"><dt>**PST \_ Não \_ substituir**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="2641a-144">Especifica que o item seja criado no armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="2641a-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="2641a-145">A substituição de um item existente não é permitida.</span><span class="sxs-lookup"><span data-stu-id="2641a-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="2641a-146"><dt>**PST \_ \_Dados não restritos**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="2641a-147">Especifica que o fluxo de dados não é seguro.</span><span class="sxs-lookup"><span data-stu-id="2641a-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="2641a-148">Por padrão, as chamadas de item são seguras.</span><span class="sxs-lookup"><span data-stu-id="2641a-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2641a-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2641a-149">Return value</span></span>

<span data-ttu-id="2641a-150">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2641a-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="2641a-151">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2641a-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2641a-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2641a-152">Requirements</span></span>



| <span data-ttu-id="2641a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="2641a-153">Requirement</span></span> | <span data-ttu-id="2641a-154">Valor</span><span class="sxs-lookup"><span data-stu-id="2641a-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2641a-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2641a-155">Header</span></span><br/> | <dl> <span data-ttu-id="2641a-156"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2641a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="2641a-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="2641a-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2641a-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2641a-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="2641a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2641a-160">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="2641a-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="2641a-161">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="2641a-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
