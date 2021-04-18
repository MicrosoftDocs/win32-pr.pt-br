---
description: Contém informações sobre um provedor de serviços de criptografia (CSP) de cartão inteligente.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Estrutura de KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752827"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="0a435-103">\_Estrutura de \_ informações do CSP do KERB SmartCard \_</span><span class="sxs-lookup"><span data-stu-id="0a435-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="0a435-104">A estrutura de **\_ informações do \_ CSP \_ do KERB SmartCard** contém informações sobre um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="0a435-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="0a435-105">Essa estrutura não é declarada em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="0a435-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a435-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a435-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="0a435-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0a435-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a435-108">**dwCspInfoLen**</span><span class="sxs-lookup"><span data-stu-id="0a435-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-109">O tamanho, em bytes, dessa estrutura, incluindo os dados anexados.</span><span class="sxs-lookup"><span data-stu-id="0a435-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="0a435-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-111">O tipo de mensagem que está sendo passada.</span><span class="sxs-lookup"><span data-stu-id="0a435-111">The type of message being passed.</span></span> <span data-ttu-id="0a435-112">Esse membro deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="0a435-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-113">**ContextInformation**</span><span class="sxs-lookup"><span data-stu-id="0a435-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0a435-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="0a435-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0a435-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-117">**sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="0a435-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0a435-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-119">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="0a435-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-120">A chave privada a ser usada do contêiner de chave especificado no buffer **bBuffer**.</span><span class="sxs-lookup"><span data-stu-id="0a435-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="0a435-121">A chave pode ser um dos seguintes valores, definidos em WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="0a435-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="0a435-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0a435-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="0a435-123">Significado</span><span class="sxs-lookup"><span data-stu-id="0a435-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="0a435-124"><dt>**Às \_ TROCA**</dt> de <dt>key1</dt></span><span class="sxs-lookup"><span data-stu-id="0a435-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="0a435-125">A chave é uma chave de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="0a435-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="0a435-126"><dt>**Às \_ ASSINATURA**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0a435-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="0a435-127">A chave é uma chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0a435-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="0a435-128">**nCardNameOffset**</span><span class="sxs-lookup"><span data-stu-id="0a435-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-129">O número de caracteres no buffer **bBuffer** que precede o nome do cartão inteligente nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="0a435-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a435-130">Se o nome do cartão inteligente não for fornecido, o buffer deverá conter uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="0a435-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="0a435-131">**nReaderNameOffset**</span><span class="sxs-lookup"><span data-stu-id="0a435-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-132">O número de caracteres no buffer **bBuffer** que precede o nome do leitor de cartão inteligente nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="0a435-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a435-133">Se o nome do leitor de cartão inteligente não for fornecido, o buffer deverá conter uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="0a435-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="0a435-134">**nContainerNameOffset**</span><span class="sxs-lookup"><span data-stu-id="0a435-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-135">O número de caracteres no buffer **bBuffer** que precede o nome do contêiner de chave nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="0a435-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="0a435-136">Esta cadeia de caracteres não pode ficar vazia.</span><span class="sxs-lookup"><span data-stu-id="0a435-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-137">**nCSPNameOffset**</span><span class="sxs-lookup"><span data-stu-id="0a435-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-138">O número de caracteres no buffer **bBuffer** que precede o nome do CSP nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="0a435-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a435-139">**bBuffer**</span><span class="sxs-lookup"><span data-stu-id="0a435-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="0a435-140">Uma matriz de caracteres inicializada com um comprimento de `sizeof(DWORD)` .</span><span class="sxs-lookup"><span data-stu-id="0a435-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="0a435-141">Esse buffer contém os nomes referenciados pelos membros **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** e **nCSPNameOffset** , bem como quaisquer dados adicionais fornecidos pelo CSP.</span><span class="sxs-lookup"><span data-stu-id="0a435-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="0a435-142">Os nomes que não são fornecidos devem ser representados nesse buffer por cadeias de caracteres vazias.</span><span class="sxs-lookup"><span data-stu-id="0a435-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a435-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a435-143">Remarks</span></span>

<span data-ttu-id="0a435-144">Quando essa estrutura é serializada, os membros da estrutura devem ser alinhados aos limites que são múltiplos de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="0a435-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a435-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a435-145">Requirements</span></span>



| <span data-ttu-id="0a435-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a435-146">Requirement</span></span> | <span data-ttu-id="0a435-147">Valor</span><span class="sxs-lookup"><span data-stu-id="0a435-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a435-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a435-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0a435-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a435-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a435-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a435-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0a435-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a435-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a435-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a435-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a435-153">**\_logon do certificado KERB \_**</span><span class="sxs-lookup"><span data-stu-id="0a435-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
