---
description: Localiza um certificado do emissor dos repositórios de certificados especificados que correspondem ao certificado de entidade especificado.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Função WTHelperCertFindIssuerCertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169685"
---
# <a name="wthelpercertfindissuercertificate-function"></a>Função WTHelperCertFindIssuerCertificate

\[A função **WTHelperCertFindIssuerCertificate** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A função **WTHelperCertFindIssuerCertificate** localiza um certificado de emissor dos repositórios de certificados especificados que correspondem ao certificado de entidade especificado.

> [!Note]  
> Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Wintrust.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pChildContext* \[ no\]
</dt> <dd>

O certificado do requerente para o qual encontrar um certificado de emissor correspondente.

</dd> <dt>

*chStores* \[ no\]
</dt> <dd>

O número de elementos na matriz *pahStores* .

</dd> <dt>

*pahStores* \[ no\]
</dt> <dd>

Uma matriz de repositórios de certificados no qual Pesquisar.

</dd> <dt>

*psftVerifyAsOf* \[ no\]
</dt> <dd>

A hora da verificação.

</dd> <dt>

*dwEncoding* \[ no\]
</dt> <dd>

Um valor **DWORD** que especifica os tipos de codificação do certificado a ser verificado. Para obter informações sobre os tipos de codificação possíveis, consulte [certificados e tipos de codificação de mensagem](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwConfidence* \[ out, opcional\]
</dt> <dd>

Esse parâmetro pode ser uma combinação de bits zero ou mais dos valores de confiança a seguir.



| Valor                                                                                                                                                                                                                                                                 | Significado                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**Certificado \_ SEGURANÇA \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | A assinatura do certificado é válida.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**Certificado \_ 0x01000000 de \_ tempo de confiança**</dt> <dt></dt> </dl>                  | A hora do emissor do certificado é válida.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt>0x00100000</dt> de <dt> **\_ \_ aninhamento de confiança de certificado**</dt> </dl>    | A hora do certificado é válida.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **\_ \_ AUTHIDEXT de confiança de certificado**</dt> <dt>0x00010000</dt> </dl> | A extensão de ID de autoridade é válida.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt>0x00001000</dt> de <dt> **\_ \_ higiene de confiança de certificado**</dt> </dl>       | No mínimo, a assinatura do certificado e a extensão da ID de autoridade são válidas.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt>0x11111000</dt> de <dt> **\_ confiança \_ máxima de certificado**</dt> </dl>       | Uma combinação de todos os outros valores de confiança.<br/>                                 |



 

</dd> <dt>

*dwError* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável **DWORD** que contém o valor de erro para esse certificado, se aplicável.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um certificado de emissor que corresponde ao certificado de entidade especificado pelo parâmetro *pChildContext* .

## <a name="remarks"></a>Comentários

Para localizar com êxito um certificado de emissor correspondente, os requisitos a seguir devem ser atendidos:

-   A assinatura do certificado da entidade especificada pelo parâmetro *pChildContext* deve ser válida.
-   O membro **rgExtension** do membro **PCertInfo** do parâmetro *pChildContext* deve conter uma estrutura de [**informações de \_ ID de chave de autoridade \_ \_ \_ de certificação**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) . Os membros **CertIssuer** e **CertSerialMember** dessa estrutura correspondem muito aos membros correspondentes para o certificado do emissor.
-   O valor do parâmetro *psftVerifyAsOf* deve estar dentro do período de validade do certificado da entidade.
-   O período de validade do certificado da entidade deve estar dentro do período de validade do certificado do emissor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
