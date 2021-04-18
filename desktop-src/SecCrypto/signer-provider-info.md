---
description: Especifica o CSP (provedor de serviços de criptografia) e as informações de chave privada usadas para criar uma assinatura digital.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Estrutura de SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778669"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="8eb0b-103">Estrutura de informações do \_ provedor de assinante \_</span><span class="sxs-lookup"><span data-stu-id="8eb0b-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="8eb0b-104">A estrutura de **\_ \_ informações do provedor de assinante** especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de chave privada usadas para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="8eb0b-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="8eb0b-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8eb0b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eb0b-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="8eb0b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8eb0b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8eb0b-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="8eb0b-111">**pwszProviderName**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-112">O nome do CSP usado para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="8eb0b-113">Se o valor desse membro for **nulo**, o provedor padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="8eb0b-114">**dwProviderType**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-115">O tipo de CSP especificado pelo membro **pwszProviderName** .</span><span class="sxs-lookup"><span data-stu-id="8eb0b-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="8eb0b-116">**dwKeySpec**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-117">A especificação de chave.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-117">The key specification.</span></span> <span data-ttu-id="8eb0b-118">Se esse membro for definido como zero, a especificação de chave no membro **pwszPvkFileName** ou **pwszKeyContainer** será usada.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="8eb0b-119">Se houver mais de uma especificação de chave no membro **pwszKeyContainer** , **a \_ assinatura** será usada.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="8eb0b-120">Se falhar, **em \_ keyexchange** será usado.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="8eb0b-121">**dwPvkChoice**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-122">Especifica o tipo de informações de chave privada.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-122">Specifies the type of private key information.</span></span> <span data-ttu-id="8eb0b-123">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="8eb0b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb0b-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="8eb0b-125">Significado</span><span class="sxs-lookup"><span data-stu-id="8eb0b-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="8eb0b-126"><dt>**PVK \_ Digite \_ o \_ nome do arquivo**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8eb0b-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="8eb0b-127">As informações de chave privada são um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="8eb0b-128"><dt>**PVK \_ Digite \_ keycontainer**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8eb0b-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8eb0b-129">As informações de chave privada são um contêiner de chave.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8eb0b-130">**pwszPvkFileName**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-131">O nome do arquivo que contém as informações de chave privada.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="8eb0b-132">**pwszKeyContainer**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="8eb0b-133">O nome do contêiner de chave que contém as informações de chave privada.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8eb0b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb0b-134">Requirements</span></span>



| <span data-ttu-id="8eb0b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb0b-135">Requirement</span></span> | <span data-ttu-id="8eb0b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb0b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8eb0b-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb0b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb0b-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8eb0b-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8eb0b-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb0b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb0b-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8eb0b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8eb0b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eb0b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb0b-142">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="8eb0b-143">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="8eb0b-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
