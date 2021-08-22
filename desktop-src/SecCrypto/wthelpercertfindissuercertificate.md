---
description: Localiza um certificado do emissor dos armazenamentos de certificado especificados que corresponde ao certificado de assunto especificado.
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
ms.openlocfilehash: 3c6c7957e969d04eaf65014e023a5f64e0826b6285fb878d9afefbd7cda25721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895828"
---
# <a name="wthelpercertfindissuercertificate-function"></a>Função WTHelperCertFindIssuerCertificate

\[A **função WTHelperCertFindIssuerCertificate** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A **função WTHelperCertFindIssuerCertificate** localiza um certificado do emissor dos armazenamentos de certificado especificados que corresponde ao certificado de assunto especificado.

> [!Note]  
> Essa função não tem nenhuma biblioteca de importação associada. Você deve usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Wintrust.dll.

 

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

*pChildContext* \[ Em\]
</dt> <dd>

O certificado de assunto para o qual encontrar um certificado de emissor correspondente.

</dd> <dt>

*chStores* \[ Em\]
</dt> <dd>

O número de elementos na matriz *pahStores.*

</dd> <dt>

*pahStores* \[ Em\]
</dt> <dd>

Uma matriz de armazenamentos de certificados nos quais pesquisar.

</dd> <dt>

*psftVerifyAsOf* \[ Em\]
</dt> <dd>

A hora da verificação.

</dd> <dt>

*dwEncoding* \[ Em\]
</dt> <dd>

Um **valor DWORD** que especifica os tipos de codificação do certificado a verificar. Para obter informações sobre possíveis tipos de codificação, consulte Tipos de codificação de [certificado e mensagem](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwConfidence* \[ out, opcional\]
</dt> <dd>

Esse parâmetro pode ser uma combinação bit a bit de zero ou mais dos valores de confiança a seguir.



| Valor                                                                                                                                                                                                                                                                 | Significado                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**CERT \_ CONFIDENCE \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | A assinatura do certificado é válida.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**CERT \_ TEMPO \_ DE CONFIANÇA**</dt> <dt> 0X01000000</dt> </dl>                  | A hora do emissor do certificado é válida.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **CERTIFICADO \_ CONFIDENCE \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | A hora do certificado é válida.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **CERTIFICADO \_ CONFIDENCE \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | A extensão de ID da autoridade é válida.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **LIMPEZA \_ DE CONFIANÇA \_ DO**</dt> <dt>CERTIFICADO 0X00001000</dt> </dl>       | No mínimo, a assinatura da extensão de ID do certificado e da autoridade é válida.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **CERTIFICADO \_ DE CONFIANÇA \_ MAIS**</dt> <dt>0X11111000</dt> </dl>       | Uma combinação de todos os outros valores de confiança.<br/>                                 |



 

</dd> <dt>

*dwError* \[ out\]
</dt> <dd>

Um ponteiro para uma **variável DWORD** que contém o valor de erro para esse certificado, se aplicável.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um certificado do emissor que corresponde ao certificado de assunto especificado pelo *parâmetro pChildContext.*

## <a name="remarks"></a>Comentários

Para encontrar com êxito um certificado do emissor correspondente, os seguintes requisitos devem ser atendidos:

-   A assinatura do certificado de assunto especificado pelo parâmetro *pChildContext* deve ser válida.
-   O **membro rgExtension** do membro **pCertInfo** do parâmetro *pChildContext* deve conter uma estrutura [**CERT AUTHORITY KEY \_ \_ \_ ID \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) Os **membros CertIssuer** e **CertSerialMember** dessa estrutura correspondem muito aos membros correspondentes para o certificado do emissor.
-   O valor do *parâmetro psftVerifyAsOf* deve estar dentro do período de validade do certificado de assunto.
-   O período de validade do certificado de assunto deve estar dentro do período de validade do certificado do emissor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
