---
description: Exclui um tipo especificado do banco de dados de armazenamento protegido.
ms.assetid: 5e3a08eb-e16b-4d9f-82be-241eb3137d17
title: 'IPStore: método eleteType de:D (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7833dd59a10b0194347e906d5c5a4711585dea14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755920"
---
# <a name="ipstoredeletetype-method"></a><span data-ttu-id="d1af1-103">IPStore: método eleteType de:D</span><span class="sxs-lookup"><span data-stu-id="d1af1-103">IPStore::DeleteType method</span></span>

<span data-ttu-id="d1af1-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1af1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d1af1-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1af1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d1af1-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="d1af1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d1af1-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d1af1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d1af1-108">Exclui um tipo especificado do banco de dados de armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="d1af1-108">Deletes a specified type from the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1af1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1af1-109">Syntax</span></span>


```C++
HRESULT DeleteType(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d1af1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1af1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1af1-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1af1-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1af1-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="d1af1-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="d1af1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d1af1-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="d1af1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d1af1-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="d1af1-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d1af1-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="d1af1-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="d1af1-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="d1af1-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d1af1-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d1af1-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="d1af1-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d1af1-119">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1af1-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1af1-120">Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d1af1-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="d1af1-121">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1af1-121">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1af1-122">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="d1af1-122">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1af1-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1af1-123">Return value</span></span>

<span data-ttu-id="d1af1-124">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1af1-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="d1af1-125">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d1af1-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1af1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1af1-126">Requirements</span></span>



| <span data-ttu-id="d1af1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1af1-127">Requirement</span></span> | <span data-ttu-id="d1af1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d1af1-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1af1-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1af1-129">Header</span></span><br/> | <dl> <span data-ttu-id="d1af1-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1af1-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d1af1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d1af1-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="d1af1-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1af1-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1af1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1af1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1af1-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="d1af1-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
