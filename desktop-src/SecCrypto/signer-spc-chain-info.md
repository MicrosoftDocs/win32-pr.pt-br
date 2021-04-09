---
description: Especifica um SPC (certificado do fornecedor de software) e uma cadeia de certificados usados para assinar um documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Estrutura de SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091621"
---
# <a name="signer_spc_chain_info-structure"></a><span data-ttu-id="a8a8f-103">\_Estrutura de \_ informações da cadeia do SPC do signatário \_</span><span class="sxs-lookup"><span data-stu-id="a8a8f-103">SIGNER\_SPC\_CHAIN\_INFO structure</span></span>

<span data-ttu-id="a8a8f-104">A estrutura de **\_ \_ \_ informações da cadeia SPC do signatário** especifica um certificado do fornecedor de [*software*](../secgloss/s-gly.md) (SPC) e uma cadeia de certificados usados para assinar um documento.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-104">The **SIGNER\_SPC\_CHAIN\_INFO** structure specifies a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) and certificate chain used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="a8a8f-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="a8a8f-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a8a8f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8a8f-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a><span data-ttu-id="a8a8f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a8a8f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8a8f-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a8a8f-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a8a8f-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="a8a8f-111">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="a8a8f-111">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="a8a8f-112">O nome do arquivo SPC a ser usado para assinar um documento.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-112">The name of the SPC file to use to sign a document.</span></span>

</dd> <dt>

<span data-ttu-id="a8a8f-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="a8a8f-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="a8a8f-114">Especifica como os certificados são adicionados à assinatura.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="a8a8f-115">Para localizar a cadeia de certificados, as lojas MY, AC, ROOT e SPC, além da loja especificada pelo membro **HCERTSTORE** , são verificadas.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="a8a8f-116">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="a8a8f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a8a8f-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="a8a8f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a8a8f-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="a8a8f-119"><dt>**Signatário \_ \_ \_ Grupo de políticas de CERT**</dt> . <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="a8a8f-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="a8a8f-120">Adicione somente certificados na cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="a8a8f-121"><dt>**Signatário \_ Cadeia de política de certificado \_ \_ \_ sem \_ raiz**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="a8a8f-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="a8a8f-122">Adicione somente certificados na cadeia de certificados, excluindo o certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="a8a8f-123"><dt>**Signatário \_ \_ \_ Repositório de política de certificado**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a8a8f-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="a8a8f-124">Adicione todos os certificados no repositório especificado pelo membro **HCERTSTORE** .</span><span class="sxs-lookup"><span data-stu-id="a8a8f-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="a8a8f-125">Esse sinalizador pode ser uma combinação bit-a-**ou** com qualquer um dos outros valores possíveis para esse membro.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a8a8f-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="a8a8f-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="a8a8f-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-127">Optional.</span></span> <span data-ttu-id="a8a8f-128">Um identificador para um repositório de certificados adicional.</span><span class="sxs-lookup"><span data-stu-id="a8a8f-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8a8f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8a8f-129">Requirements</span></span>



| <span data-ttu-id="a8a8f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8a8f-130">Requirement</span></span> | <span data-ttu-id="a8a8f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a8a8f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8a8f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8a8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a8f-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8a8f-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a8a8f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8a8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a8f-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8a8f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8a8f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8a8f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a8f-137">**certificado do ASSINAnte \_**</span><span class="sxs-lookup"><span data-stu-id="a8a8f-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 
