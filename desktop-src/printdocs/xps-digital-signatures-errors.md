---
description: A tabela a seguir lista todos os valores HRESULT que podem ser retornados pelos métodos na API de Assinatura Digital XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Erros de API de Assinatura Digital XPS (Xpsdigitalsignature.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e40cea4b7d0e9997157c8b18c7f364ac7ac58b2b9edc6faec62cbe98685fcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711356"
---
# <a name="xps-digital-signature-api-errors"></a>Erros da API de Assinatura Digital XPS

A tabela a seguir lista todos **os valores HRESULT** que podem ser retornados pelos métodos na API de Assinatura Digital XPS. Observe que nem todos os métodos podem retornar todos os valores de retorno listados nesta tabela.



| Valor/código de retorno                                                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                                                                                                                 | O método foi bem-sucedido.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ ASSINATURA \_ INVÁLIDABLOQUEAR \_ MARCAÇÃO**</dt> <dt>0X8052038B</dt> </dl> | Encontrou um erro na marcação XML do bloco de assinatura enquanto a marcação de assinatura estava sendo lida.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ ELEMENTOS \_ DE \_ COMPATIBILIDADE DE \_ MARCAÇÃO**</dt> <dt>E 0X80520389</dt> </dl> | O [**valor \_ DE SINALIZADORES DE SINAL \_ XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) especificou que nenhum elemento de compatibilidade de marcação era esperado; no entanto, os elementos de compatibilidade de marcação foram encontrados.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E \_ OBJECT \_ DETACHED**</dt> <dt>0x8052038a</dt> </dl>                                            | A interface não está associada ao gerenciador de assinaturas.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ PACOTE E \_ \_ JÁ ABERTO \_ 0X80520387**</dt> <dt></dt> </dl>                      | Um pacote XPS já foi aberto no gerenciador de assinaturas. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ PACOTE E \_ \_ NÃO ABERTO \_ 0X80520386**</dt> <dt></dt> </dl>                                  | Um pacote XPS ainda não foi aberto no gerenciador de assinaturas. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Duas ou mais assinaturas têm a mesma ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | A ID da solicitação de assinatura não é exclusiva dentro do bloco de assinatura.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentários

Alguns métodos de API de assinatura digital XPS fazem chamadas para a API [de Empacotamento.](/previous-versions/windows/desktop/opc/packaging) Para obter informações sobre os valores de retorno da API de Empacotamento, consulte [Erros de empacotamento](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                            |
| Cabeçalho<br/>                   | <dl> <dt>Xpsdigitalsignature.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>XpsDigitalSignature.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tratamento de erro em COM](../com/error-handling-in-com.md)
</dt> <dt>

[Erros de empacotamento](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valores de retorno de criptografia](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

