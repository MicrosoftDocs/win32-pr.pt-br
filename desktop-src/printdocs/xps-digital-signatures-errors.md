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
# <a name="xps-digital-signature-api-errors"></a>Erros de API de assinatura digital XPS

A tabela a seguir lista todos os valores **HRESULT** que podem ser retornados pelos métodos na API de assinatura digital XPS. Observe que nem todos os métodos podem retornar cada valor de retorno listado nesta tabela.



| Código/valor de retorno                                                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                                                                                                                 | O método foi bem-sucedido.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E 0x8052038b de \_ \_ \_ marcação SIGNATUREBLOCK inválida**</dt> <dt></dt> </dl> | Erro encontrado na marcação XML do bloco de assinatura enquanto a marcação de assinatura estava sendo lida.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ \_Elementos de \_ compatibilidade \_ de marcação E**</dt> <dt>0x80520389</dt> </dl> | O valor dos [**\_ \_ sinalizadores de sinal de XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) especificou que nenhum elemento de compatibilidade de marcação era esperado; no entanto, foram encontrados elementos de compatibilidade de marcação.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ \_Objeto E \_ desanexado**</dt> <dt>0x8052038a</dt> </dl>                                            | A interface não está associada ao Gerenciador de assinatura.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ \_Pacote E \_ já \_ aberto**</dt> <dt>0x80520387</dt> </dl>                      | Um pacote XPS já foi aberto no Gerenciador de assinaturas. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ \_Pacote E \_ não \_ aberto**</dt> <dt>0x80520386</dt> </dl>                                  | Um pacote XPS ainda não foi aberto no Gerenciador de assinaturas. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ signatureId \_ dup**</dt> <dt>0x80520388</dt> </dl>                                            | Duas ou mais assinaturas têm a mesma ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ dup**</dt> <dt>0x80520385</dt> </dl>                                         | A ID da solicitação de assinatura não é exclusiva dentro do bloco de assinatura.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentários

Alguns métodos de API de assinatura digital XPS fazem chamadas para a API de [empacotamento](/previous-versions/windows/desktop/opc/packaging) . Para obter informações sobre os valores de retorno da API de empacotamento, consulte [erros de empacotamento](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                            |
| parâmetro<br/>                   | <dl> <dt>XpsDigitalSignature. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>XpsDigitalSignature. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tratamento de erro em COM](../com/error-handling-in-com.md)
</dt> <dt>

[Erros de empacotamento](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valores de retorno de criptografia](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

