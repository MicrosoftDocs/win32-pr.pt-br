---
description: Cria o tipo especificado com o nome especificado.
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: 'Método IPStore:: CreateType (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7a8c855fd5b50adf41986ef27a1bd296894b12bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752569"
---
# <a name="ipstorecreatetype-method"></a><span data-ttu-id="6acb9-103">Método IPStore:: CreateType</span><span class="sxs-lookup"><span data-stu-id="6acb9-103">IPStore::CreateType method</span></span>

<span data-ttu-id="6acb9-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6acb9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6acb9-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6acb9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6acb9-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="6acb9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6acb9-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6acb9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6acb9-108">Cria o tipo especificado com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="6acb9-108">Creates the specified type with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6acb9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6acb9-109">Syntax</span></span>


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6acb9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6acb9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6acb9-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6acb9-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6acb9-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="6acb9-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="6acb9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6acb9-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="6acb9-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6acb9-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="6acb9-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="6acb9-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="6acb9-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="6acb9-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="6acb9-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6acb9-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6acb9-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="6acb9-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6acb9-119">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6acb9-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6acb9-120">Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6acb9-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="6acb9-121">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6acb9-121">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6acb9-122">Um ponteiro para uma estrutura de [**\_ TYPEINFO de PST**](pst-typeinfo.md) que contém o nome do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6acb9-122">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure that contains the name of the data type.</span></span>

</dd> <dt>

<span data-ttu-id="6acb9-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6acb9-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6acb9-124">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6acb9-124">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6acb9-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6acb9-125">Return value</span></span>

<span data-ttu-id="6acb9-126">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6acb9-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="6acb9-127">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6acb9-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6acb9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6acb9-128">Requirements</span></span>



| <span data-ttu-id="6acb9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6acb9-129">Requirement</span></span> | <span data-ttu-id="6acb9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6acb9-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6acb9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6acb9-131">Header</span></span><br/> | <dl> <span data-ttu-id="6acb9-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6acb9-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6acb9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6acb9-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="6acb9-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6acb9-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6acb9-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6acb9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6acb9-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6acb9-136">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="6acb9-137">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="6acb9-137">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
