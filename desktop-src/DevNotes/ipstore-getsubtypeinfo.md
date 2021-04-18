---
description: Recupera informações associadas a um subtipo.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'Método IPStore:: GetSubtypeInfo (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: db7cb02d1c21b8bb1717514a6347339065e4f112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753061"
---
# <a name="ipstoregetsubtypeinfo-method"></a><span data-ttu-id="aaa04-103">Método IPStore:: GetSubtypeInfo</span><span class="sxs-lookup"><span data-stu-id="aaa04-103">IPStore::GetSubtypeInfo method</span></span>

<span data-ttu-id="aaa04-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aaa04-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="aaa04-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="aaa04-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="aaa04-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="aaa04-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="aaa04-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="aaa04-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="aaa04-108">Recupera informações associadas a um subtipo.</span><span class="sxs-lookup"><span data-stu-id="aaa04-108">Retrieves information associated with a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa04-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaa04-109">Syntax</span></span>


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="aaa04-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaa04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa04-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaa04-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa04-112">A área de armazenamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="aaa04-112">The provider storage area.</span></span>



| <span data-ttu-id="aaa04-113">Valor</span><span class="sxs-lookup"><span data-stu-id="aaa04-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="aaa04-114">Significado</span><span class="sxs-lookup"><span data-stu-id="aaa04-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="aaa04-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="aaa04-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="aaa04-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="aaa04-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="aaa04-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="aaa04-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="aaa04-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="aaa04-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aaa04-119">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaa04-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa04-120">Um ponteiro para um GUID que identifica o tipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aaa04-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="aaa04-121">*pSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaa04-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa04-122">Um ponteiro para um GUID que identifica o subtipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aaa04-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="aaa04-123">*ppInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaa04-123">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa04-124">Um ponteiro para uma estrutura de [**\_ TYPEINFO de PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="aaa04-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aaa04-125">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaa04-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa04-126">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="aaa04-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa04-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aaa04-127">Return value</span></span>

<span data-ttu-id="aaa04-128">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aaa04-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="aaa04-129">Um valor de PST \_ E \_ OK indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aaa04-129">A value of PST\_E\_OK indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa04-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaa04-130">Requirements</span></span>



| <span data-ttu-id="aaa04-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaa04-131">Requirement</span></span> | <span data-ttu-id="aaa04-132">Valor</span><span class="sxs-lookup"><span data-stu-id="aaa04-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa04-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aaa04-133">Header</span></span><br/> | <dl> <span data-ttu-id="aaa04-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa04-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="aaa04-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aaa04-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="aaa04-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaa04-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa04-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaa04-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa04-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="aaa04-138">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="aaa04-139">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="aaa04-139">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
