---
description: Retorna uma interface para enumerar tipos que estão atualmente registrados no banco de dados protegido.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: 'Método IPStore:: EnumTypes (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73166a9fc1d76ae9f67528636eda567b9fa190a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750543"
---
# <a name="ipstoreenumtypes-method"></a><span data-ttu-id="965c6-103">Método IPStore:: EnumTypes</span><span class="sxs-lookup"><span data-stu-id="965c6-103">IPStore::EnumTypes method</span></span>

<span data-ttu-id="965c6-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="965c6-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="965c6-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="965c6-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="965c6-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="965c6-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="965c6-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="965c6-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="965c6-108">Retorna uma interface para enumerar tipos que estão atualmente registrados no banco de dados protegido.</span><span class="sxs-lookup"><span data-stu-id="965c6-108">Returns an interface for enumerating types that are currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="965c6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="965c6-109">Syntax</span></span>


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="965c6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="965c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965c6-111">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="965c6-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965c6-112">Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.</span><span class="sxs-lookup"><span data-stu-id="965c6-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="965c6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="965c6-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="965c6-114">Significado</span><span class="sxs-lookup"><span data-stu-id="965c6-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="965c6-115"><dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="965c6-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="965c6-116">O armazenamento é mantido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="965c6-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="965c6-117"><dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="965c6-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="965c6-118">O armazenamento é mantido na seção máquina local do registro.</span><span class="sxs-lookup"><span data-stu-id="965c6-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="965c6-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="965c6-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965c6-120">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="965c6-120">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="965c6-121">*ppEnum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="965c6-121">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965c6-122">Um ponteiro para uma interface [**IEnumPStoreTypes**](ienumpstoretypes.md) que é usada para executar as tarefas de enumeração.</span><span class="sxs-lookup"><span data-stu-id="965c6-122">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to perform the enumeration tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965c6-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="965c6-123">Return value</span></span>

<span data-ttu-id="965c6-124">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="965c6-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="965c6-125">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="965c6-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="965c6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="965c6-126">Requirements</span></span>



| <span data-ttu-id="965c6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="965c6-127">Requirement</span></span> | <span data-ttu-id="965c6-128">Valor</span><span class="sxs-lookup"><span data-stu-id="965c6-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="965c6-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="965c6-129">Header</span></span><br/> | <dl> <span data-ttu-id="965c6-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="965c6-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="965c6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="965c6-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="965c6-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="965c6-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965c6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="965c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965c6-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="965c6-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
