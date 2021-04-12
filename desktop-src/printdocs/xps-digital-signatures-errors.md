---
description: A tabela a seguir lista todos os valores HRESULT que podem ser retornados pelos métodos na API de assinatura digital XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Erros de API de assinatura digital XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297291"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="41560-103">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="41560-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="41560-104">A tabela a seguir lista todos os valores **HRESULT** que podem ser retornados pelos métodos na API de assinatura digital XPS.</span><span class="sxs-lookup"><span data-stu-id="41560-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="41560-105">Observe que nem todos os métodos podem retornar cada valor de retorno listado nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="41560-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="41560-106">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="41560-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="41560-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="41560-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="41560-108"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41560-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="41560-109">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="41560-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="41560-110"><dt>**XPS \_ E 0x8052038b de \_ \_ \_ marcação SIGNATUREBLOCK inválida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="41560-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="41560-111">Erro encontrado na marcação XML do bloco de assinatura enquanto a marcação de assinatura estava sendo lida.</span><span class="sxs-lookup"><span data-stu-id="41560-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="41560-112"><dt>**XPS \_ \_Elementos de \_ compatibilidade \_ de marcação E**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="41560-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="41560-113">O valor dos [**\_ \_ sinalizadores de sinal de XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) especificou que nenhum elemento de compatibilidade de marcação era esperado; no entanto, foram encontrados elementos de compatibilidade de marcação.</span><span class="sxs-lookup"><span data-stu-id="41560-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="41560-114"><dt>**XPS \_ \_Objeto E \_ desanexado**</dt> <dt>0x8052038a</dt></span><span class="sxs-lookup"><span data-stu-id="41560-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="41560-115">A interface não está associada ao Gerenciador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="41560-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="41560-116"><dt>**XPS \_ \_Pacote E \_ já \_ aberto**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="41560-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="41560-117">Um pacote XPS já foi aberto no Gerenciador de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="41560-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="41560-118"><dt>**XPS \_ \_Pacote E \_ não \_ aberto**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="41560-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="41560-119">Um pacote XPS ainda não foi aberto no Gerenciador de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="41560-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="41560-120"><dt>**XPS \_ E \_ signatureId \_ dup**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="41560-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="41560-121">Duas ou mais assinaturas têm a mesma ID.</span><span class="sxs-lookup"><span data-stu-id="41560-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="41560-122"><dt>**XPS \_ E \_ SIGREQUESTID \_ dup**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="41560-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="41560-123">A ID da solicitação de assinatura não é exclusiva dentro do bloco de assinatura.</span><span class="sxs-lookup"><span data-stu-id="41560-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="41560-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="41560-124">Remarks</span></span>

<span data-ttu-id="41560-125">Alguns métodos de API de assinatura digital XPS fazem chamadas para a API de [empacotamento](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="41560-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="41560-126">Para obter informações sobre os valores de retorno da API de empacotamento, consulte [erros de empacotamento](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="41560-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="41560-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41560-127">Requirements</span></span>



| <span data-ttu-id="41560-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="41560-128">Requirement</span></span> | <span data-ttu-id="41560-129">Valor</span><span class="sxs-lookup"><span data-stu-id="41560-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41560-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41560-130">Minimum supported client</span></span><br/> | <span data-ttu-id="41560-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="41560-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="41560-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41560-132">Minimum supported server</span></span><br/> | <span data-ttu-id="41560-133">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="41560-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="41560-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41560-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="41560-135"><dt>XpsDigitalSignature. h</dt></span><span class="sxs-lookup"><span data-stu-id="41560-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="41560-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="41560-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41560-137"><dt>XpsDigitalSignature. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41560-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41560-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="41560-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41560-139">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="41560-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="41560-140">Erros de empacotamento</span><span class="sxs-lookup"><span data-stu-id="41560-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="41560-141">Valores de retorno de criptografia</span><span class="sxs-lookup"><span data-stu-id="41560-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

