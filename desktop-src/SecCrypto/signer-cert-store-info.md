---
description: Especifica o repositório de certificados usado para assinar um documento.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Estrutura de SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767818"
---
# <a name="signer_cert_store_info-structure"></a><span data-ttu-id="9ac17-103">\_Estrutura de \_ informações do repositório de certificados do assinante \_</span><span class="sxs-lookup"><span data-stu-id="9ac17-103">SIGNER\_CERT\_STORE\_INFO structure</span></span>

<span data-ttu-id="9ac17-104">A estrutura de informações do repositório de certificados do signatário especifica o repositório de certificados usado para assinar um documento. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ac17-104">The **SIGNER\_CERT\_STORE\_INFO** structure specifies the certificate store used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="9ac17-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9ac17-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="9ac17-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9ac17-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9ac17-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ac17-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a><span data-ttu-id="9ac17-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9ac17-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ac17-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="9ac17-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="9ac17-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="9ac17-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ac17-111">**pSigningCert**</span><span class="sxs-lookup"><span data-stu-id="9ac17-111">**pSigningCert**</span></span>
</dt> <dd>

<span data-ttu-id="9ac17-112">Um ponteiro para uma estrutura de [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="9ac17-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="9ac17-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="9ac17-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="9ac17-114">Especifica como os certificados são adicionados à assinatura.</span><span class="sxs-lookup"><span data-stu-id="9ac17-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="9ac17-115">Para localizar a cadeia de certificados, as lojas MY, AC, ROOT e SPC, além da loja especificada pelo membro **HCERTSTORE** , são verificadas.</span><span class="sxs-lookup"><span data-stu-id="9ac17-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="9ac17-116">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ac17-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="9ac17-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9ac17-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="9ac17-118">Significado</span><span class="sxs-lookup"><span data-stu-id="9ac17-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="9ac17-119"><dt>**Signatário \_ \_ \_ Grupo de políticas de CERT**</dt> . <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="9ac17-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="9ac17-120">Adicione somente certificados na cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ac17-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="9ac17-121"><dt>**Signatário \_ Cadeia de política de certificado \_ \_ \_ sem \_ raiz**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="9ac17-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="9ac17-122">Adicione somente certificados na cadeia de certificados, excluindo o certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="9ac17-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="9ac17-123"><dt>**Signatário \_ \_ \_ Repositório de política de certificado**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="9ac17-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="9ac17-124">Adicione todos os certificados no repositório especificado pelo membro **HCERTSTORE** .</span><span class="sxs-lookup"><span data-stu-id="9ac17-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="9ac17-125">Esse sinalizador pode ser uma combinação bit-a-**ou** com qualquer um dos outros valores possíveis para esse membro.</span><span class="sxs-lookup"><span data-stu-id="9ac17-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9ac17-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="9ac17-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="9ac17-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9ac17-127">Optional.</span></span> <span data-ttu-id="9ac17-128">Um identificador para um repositório de certificados adicional.</span><span class="sxs-lookup"><span data-stu-id="9ac17-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ac17-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ac17-129">Requirements</span></span>



| <span data-ttu-id="9ac17-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ac17-130">Requirement</span></span> | <span data-ttu-id="9ac17-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9ac17-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9ac17-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ac17-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac17-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ac17-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9ac17-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ac17-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac17-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ac17-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ac17-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ac17-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac17-137">**certificado do ASSINAnte \_**</span><span class="sxs-lookup"><span data-stu-id="9ac17-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 




