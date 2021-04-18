---
description: Abre um item para vários acessos.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Método IPStore:: OpenItem (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751038"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="89589-103">Método IPStore:: OpenItem</span><span class="sxs-lookup"><span data-stu-id="89589-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="89589-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89589-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="89589-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="89589-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="89589-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="89589-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="89589-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="89589-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="89589-108">Abre um item para vários acessos.</span><span class="sxs-lookup"><span data-stu-id="89589-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="89589-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89589-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="89589-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89589-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89589-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="89589-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="89589-113">Valor</span><span class="sxs-lookup"><span data-stu-id="89589-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="89589-114">Significado</span><span class="sxs-lookup"><span data-stu-id="89589-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="89589-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="89589-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="89589-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="89589-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="89589-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="89589-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="89589-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="89589-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="89589-119">*pItemType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-120">Um ponteiro para um GUID que identifica o tipo de dados do item a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="89589-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="89589-121">*pItemSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-122">Um ponteiro para um GUID que indica o subtipo de item a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="89589-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="89589-123">*szItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-124">Uma cadeia de caracteres que contém o nome do item a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="89589-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="89589-125">*ModeFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-126">Descreve os modos de acesso aos quais um conjunto especificado de cláusulas de acesso pertence.</span><span class="sxs-lookup"><span data-stu-id="89589-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="89589-127">Para obter mais informações, consulte [**Pstore Types**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="89589-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="89589-128">Valor</span><span class="sxs-lookup"><span data-stu-id="89589-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="89589-129">Significado</span><span class="sxs-lookup"><span data-stu-id="89589-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="89589-130"><dt>**PST \_ LER**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="89589-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="89589-131">Modo de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="89589-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="89589-132"><dt>**PST \_**</dt> <dt>0X0002</dt> de gravação</span><span class="sxs-lookup"><span data-stu-id="89589-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="89589-133">Modo de acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="89589-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="89589-134">*pProomptInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-135">Um ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="89589-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="89589-136">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89589-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89589-137">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="89589-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89589-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89589-138">Return value</span></span>

<span data-ttu-id="89589-139">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89589-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="89589-140">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="89589-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="89589-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="89589-141">Remarks</span></span>

<span data-ttu-id="89589-142">Usar **OpenItem** para abrir um item no banco de dados de armazenamento protegido requer que ele eventualmente seja fechado usando [**IPStore:: CloseItem**](ipstore-closeitem.md) para evitar um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="89589-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="89589-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89589-143">Requirements</span></span>



| <span data-ttu-id="89589-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="89589-144">Requirement</span></span> | <span data-ttu-id="89589-145">Valor</span><span class="sxs-lookup"><span data-stu-id="89589-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89589-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89589-146">Header</span></span><br/> | <dl> <span data-ttu-id="89589-147"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="89589-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="89589-148">DLL</span><span class="sxs-lookup"><span data-stu-id="89589-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="89589-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89589-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89589-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="89589-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89589-151">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="89589-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="89589-152">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="89589-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
