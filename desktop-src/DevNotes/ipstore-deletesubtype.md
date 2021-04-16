---
description: Exclui um subtipo especificado de dentro do tipo especificado.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: 'IPStore: método eleteSubtype de:D (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 6fd89c1dd00a71cb843596e08bc168b90008b180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747677"
---
# <a name="ipstoredeletesubtype-method"></a><span data-ttu-id="7cb4e-103">IPStore: método eleteSubtype de:D</span><span class="sxs-lookup"><span data-stu-id="7cb4e-103">IPStore::DeleteSubtype method</span></span>

<span data-ttu-id="7cb4e-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7cb4e-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7cb4e-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7cb4e-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="7cb4e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7cb4e-108">Exclui um subtipo especificado de dentro do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-108">Deletes a specified subtype from within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb4e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cb4e-109">Syntax</span></span>


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7cb4e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cb4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb4e-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cb4e-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb4e-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="7cb4e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb4e-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="7cb4e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="7cb4e-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="7cb4e-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="7cb4e-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="7cb4e-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="7cb4e-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7cb4e-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7cb4e-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7cb4e-119">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cb4e-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb4e-120">Um ponteiro para um GUID que identifica o tipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="7cb4e-121">*pSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cb4e-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb4e-122">Um ponteiro para um GUID que identifica o subtipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="7cb4e-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cb4e-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb4e-124">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-124">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cb4e-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cb4e-125">Return value</span></span>

<span data-ttu-id="7cb4e-126">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cb4e-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="7cb4e-127">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7cb4e-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb4e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cb4e-128">Requirements</span></span>



| <span data-ttu-id="7cb4e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cb4e-129">Requirement</span></span> | <span data-ttu-id="7cb4e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb4e-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb4e-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cb4e-131">Header</span></span><br/> | <dl> <span data-ttu-id="7cb4e-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cb4e-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="7cb4e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7cb4e-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="7cb4e-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cb4e-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb4e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cb4e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb4e-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="7cb4e-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
