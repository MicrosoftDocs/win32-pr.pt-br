---
description: Especifica um certificado usado para assinar um documento. O certificado pode ser armazenado em um arquivo de certificado do fornecedor de software (SPC) ou em um repositório de certificados.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Estrutura de SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171107"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="702ce-104">Estrutura do certificado do ASSINAnte \_</span><span class="sxs-lookup"><span data-stu-id="702ce-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="702ce-105">A estrutura de **\_ certificado do signatário** especifica um [*certificado*](../secgloss/c-gly.md) usado para assinar um documento.</span><span class="sxs-lookup"><span data-stu-id="702ce-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="702ce-106">O certificado pode ser armazenado em um arquivo de [*certificado do fornecedor de software*](../secgloss/s-gly.md) (SPC) ou em um repositório de [*certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="702ce-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="702ce-107">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="702ce-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="702ce-108">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="702ce-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="702ce-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="702ce-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="702ce-110">Membros</span><span class="sxs-lookup"><span data-stu-id="702ce-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="702ce-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="702ce-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="702ce-112">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="702ce-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="702ce-113">**dwCertChoice**</span><span class="sxs-lookup"><span data-stu-id="702ce-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="702ce-114">Especifica como o certificado é armazenado.</span><span class="sxs-lookup"><span data-stu-id="702ce-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="702ce-115">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="702ce-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="702ce-116">Valor</span><span class="sxs-lookup"><span data-stu-id="702ce-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="702ce-117">Significado</span><span class="sxs-lookup"><span data-stu-id="702ce-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="702ce-118"><dt>**Signatário \_ \_ \_ Arquivo SPC do certificado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="702ce-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="702ce-119">O certificado é armazenado em um arquivo SPC.</span><span class="sxs-lookup"><span data-stu-id="702ce-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="702ce-120">O membro **pwszSpcFile** contém o caminho e o nome do arquivo do SPC.</span><span class="sxs-lookup"><span data-stu-id="702ce-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="702ce-121"><dt>**Signatário \_ \_Repositório de certificados**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="702ce-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="702ce-122">O certificado é armazenado em um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="702ce-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="702ce-123">O membro **pCertStoreInfo** contém um ponteiro para uma estrutura de informações de [**repositório de certificados de assinante \_ \_ \_**](signer-cert-store-info.md) que especifica o repositório de certificados no qual o certificado é armazenado.</span><span class="sxs-lookup"><span data-stu-id="702ce-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="702ce-124"><dt>**Signatário \_ \_ \_ Cadeia SPC do certificado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="702ce-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="702ce-125">O certificado é armazenado em um arquivo SPC e está associado a uma cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="702ce-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="702ce-126">O membro **pSpcChainInfo** contém um ponteiro para uma estrutura de informações de cadeia do SPC de [**signatário \_ \_ \_**](signer-spc-chain-info.md) que contém as informações de cadeia para o certificado.</span><span class="sxs-lookup"><span data-stu-id="702ce-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="702ce-127">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="702ce-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="702ce-128">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o caminho e o nome do arquivo do SPC no qual o certificado é armazenado.</span><span class="sxs-lookup"><span data-stu-id="702ce-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="702ce-129">Esse membro só será usado se o membro **dwCertChoice** contiver o **\_ \_ \_ arquivo SPC do certificado do signatário**.</span><span class="sxs-lookup"><span data-stu-id="702ce-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="702ce-130">**pCertStoreInfo**</span><span class="sxs-lookup"><span data-stu-id="702ce-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="702ce-131">Um ponteiro para uma estrutura de [**\_ informações de repositório de certificados \_ \_ de assinante**](signer-cert-store-info.md) que especifica o repositório de certificados no qual o certificado é armazenado.</span><span class="sxs-lookup"><span data-stu-id="702ce-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="702ce-132">Esse membro só será usado se o membro **dwCertChoice** contiver **\_ \_ repositório de certificados de assinante**.</span><span class="sxs-lookup"><span data-stu-id="702ce-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="702ce-133">**pSpcChainInfo**</span><span class="sxs-lookup"><span data-stu-id="702ce-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="702ce-134">Um ponteiro para uma estrutura de informações de cadeia do SPC de signatário que contém as informações de cadeia do certificado. [**\_ \_ \_**](signer-spc-chain-info.md)</span><span class="sxs-lookup"><span data-stu-id="702ce-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="702ce-135">Esse membro só será usado se o membro **dwCertChoice** contiver uma **\_ \_ \_ cadeia SPC do certificado do assinante**.</span><span class="sxs-lookup"><span data-stu-id="702ce-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="702ce-136">**HWND**</span><span class="sxs-lookup"><span data-stu-id="702ce-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="702ce-137">O identificador da janela a ser usada como o proprietário de qualquer caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="702ce-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="702ce-138">Esse membro não é usado no momento e é ignorado.</span><span class="sxs-lookup"><span data-stu-id="702ce-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="702ce-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="702ce-139">Requirements</span></span>



| <span data-ttu-id="702ce-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="702ce-140">Requirement</span></span> | <span data-ttu-id="702ce-141">Valor</span><span class="sxs-lookup"><span data-stu-id="702ce-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="702ce-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="702ce-142">Minimum supported client</span></span><br/> | <span data-ttu-id="702ce-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="702ce-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="702ce-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="702ce-144">Minimum supported server</span></span><br/> | <span data-ttu-id="702ce-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="702ce-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="702ce-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="702ce-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702ce-147">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="702ce-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="702ce-148">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="702ce-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
