---
description: Lê o item de dados especificado do armazenamento protegido.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Método IPStore:: ReadItem (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755279"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="fdb62-103">Método IPStore:: ReadItem</span><span class="sxs-lookup"><span data-stu-id="fdb62-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="fdb62-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fdb62-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fdb62-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fdb62-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fdb62-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="fdb62-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fdb62-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fdb62-108">Lê o item de dados especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="fdb62-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb62-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdb62-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fdb62-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdb62-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb62-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-112">A área de armazenamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="fdb62-112">The provider storage area.</span></span>



| <span data-ttu-id="fdb62-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fdb62-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="fdb62-114">Significado</span><span class="sxs-lookup"><span data-stu-id="fdb62-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="fdb62-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="fdb62-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="fdb62-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="fdb62-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="fdb62-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="fdb62-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fdb62-119">*pItemType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-120">Um ponteiro para um GUID que identifica o tipo de dados do item a ser lido.</span><span class="sxs-lookup"><span data-stu-id="fdb62-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="fdb62-121">*pItemSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-122">Um ponteiro para um GUID que identifica o subtipo de dados do item a ser lido.</span><span class="sxs-lookup"><span data-stu-id="fdb62-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="fdb62-123">*szItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-124">Um ponteiro para uma cadeia de caracteres que contém o nome atribuído ao item de dados armazenado.</span><span class="sxs-lookup"><span data-stu-id="fdb62-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="fdb62-125">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-126">Um **DWORD** que indica o tamanho do buffer que contém o item de dados armazenado.</span><span class="sxs-lookup"><span data-stu-id="fdb62-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="fdb62-127">*pbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-128">Um ponteiro para um buffer que contém o item de dados armazenado.</span><span class="sxs-lookup"><span data-stu-id="fdb62-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="fdb62-129">*pPromptInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-130">Um ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="fdb62-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fdb62-131">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdb62-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb62-132">Especifica a interface do usuário e os comportamentos de segurança para a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="fdb62-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="fdb62-133">Os valores de sinalizador podem ser combinados com um OR lógico.</span><span class="sxs-lookup"><span data-stu-id="fdb62-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="fdb62-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fdb62-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="fdb62-135">Significado</span><span class="sxs-lookup"><span data-stu-id="fdb62-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="fdb62-136"><dt>**PST \_ \_Dados não restritos**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="fdb62-137">Especifica que o fluxo de dados não é seguro.</span><span class="sxs-lookup"><span data-stu-id="fdb62-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="fdb62-138">Por padrão, as chamadas de item são seguras.</span><span class="sxs-lookup"><span data-stu-id="fdb62-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="fdb62-139"><dt>**PST \_ 0x00000008 de \_ consulta de prompt**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="fdb62-140">Especifica que a confirmação será retornada após o êxito.</span><span class="sxs-lookup"><span data-stu-id="fdb62-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="fdb62-141">Se a interface do usuário estiver habilitada, um sucesso do **PST \_ E \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="fdb62-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="fdb62-142">Se a interface do usuário não estiver habilitada, um valor de **PST \_ E \_ item \_ existente** será retornado.</span><span class="sxs-lookup"><span data-stu-id="fdb62-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="fdb62-143"><dt>**PST \_ NENHUMA \_ \_ migração de interface do usuário**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="fdb62-144">Não mostrar interface do usuário, a menos que uma senha personalizada seja necessária.</span><span class="sxs-lookup"><span data-stu-id="fdb62-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb62-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdb62-145">Return value</span></span>

<span data-ttu-id="fdb62-146">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fdb62-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="fdb62-147">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fdb62-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdb62-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdb62-148">Remarks</span></span>

<span data-ttu-id="fdb62-149">Se o **ReadItem** for concluído com êxito, o aplicativo será responsável por liberar o buffer de dados retornado usando a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .</span><span class="sxs-lookup"><span data-stu-id="fdb62-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb62-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdb62-150">Requirements</span></span>



| <span data-ttu-id="fdb62-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdb62-151">Requirement</span></span> | <span data-ttu-id="fdb62-152">Valor</span><span class="sxs-lookup"><span data-stu-id="fdb62-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb62-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdb62-153">Header</span></span><br/> | <dl> <span data-ttu-id="fdb62-154"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="fdb62-155">DLL</span><span class="sxs-lookup"><span data-stu-id="fdb62-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="fdb62-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdb62-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdb62-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdb62-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb62-158">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="fdb62-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="fdb62-159">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="fdb62-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
