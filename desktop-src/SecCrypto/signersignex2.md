---
description: Os sinais e a hora carimbam o arquivo especificado, permitindo várias assinaturas aninhadas.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: Função SignerSignEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171106"
---
# <a name="signersignex2-function"></a>Função SignerSignEx2

A função **SignerSignEx2** sinaliza e o tempo marca o arquivo especificado, permitindo várias assinaturas aninhadas.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Modifica o comportamento dessa função.

Se o arquivo a ser assinado for um arquivo executável portátil (PE), isso poderá ser zero ou uma combinação de um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_ \_ \_ \_ Sinalizador de hashes de página do PE do exc**</dt> <dt></dt> </dl>                    | Exclua os hashes de página ao criar dados indiretos SIP para o arquivo PE. Esse sinalizador tem precedência sobre o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** .<br/> Se nem o sinalizador de **\_ \_ \_ \_ hashes \_ de página do SPC exc PE** ou o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** . do SPC for especificado, o valor definido com a função [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) será usado para essa configuração. O padrão para essa configuração é excluir hashes de página ao criar dados indiretos SIP para arquivos PE.<br/> Esse valor é definido no arquivo de cabeçalho Mssip. h.<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ \_Sinalizador de \_ \_ tabela de \_ \_ end de importação do PE Inc**</dt> <dt></dt> </dl> | Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ 0x40 \_ do \_ \_ \_ sinalizador de informações de depuração Inc PE**</dt> <dt></dt> </dl>                       | Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ 0x80 \_ de \_ \_ sinalizador de recursos do PE Inc**</dt> <dt></dt> </dl>                           | Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ 0x100 \_ do \_ \_ \_ sinalizador de hash da página do PE Inc**</dt> <dt></dt> </dl>                   | Inclua hashes de página ao criar dados indiretos SIP para o arquivo PE.<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> Esse valor é definido no arquivo de cabeçalho Mssip. h.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**SIG \_ ACRESCENTAR**</dt> <dt>0x1000</dt> </dl>                                                                         | A assinatura será aninhada. Se você definir esse sinalizador antes que qualquer assinatura tenha sido adicionada, a assinatura gerada será adicionada como a assinatura externa. Se você não definir esse sinalizador, a assinatura gerada substituirá a assinatura externa, excluindo todas as assinaturas internas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pSubjectInfo* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que especifica o assunto a ser assinado.

</dd> <dt>

*pSignerCert* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ certificado de signatário**](signer-cert.md) que especifica o certificado a ser usado para criar a assinatura digital.

</dd> <dt>

*pSignatureInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de assinatura de assinante**](signer-signature-info.md) que contém informações sobre a assinatura digital.

</dd> <dt>

*pProviderInfo* \[ em, opcional\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ informações do provedor de assinante**](signer-provider-info.md) que especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de chave privada usadas para criar a assinatura digital.

Se o valor desse parâmetro for **nulo**, o parâmetro *pSignerCert* deverá especificar um certificado associado a um CSP.

</dd> <dt>

*dwTimestampFlags* \[ em, opcional\]
</dt> <dd>

Sinalizadores que serão passados para [**SignerTimeStampEx3**](signertimestampex3.md) se o parâmetro *PwszHttpTimeStamp* não for **nulo**. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                          | Significado                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**\_carimbo de data/hora do signatário \_ AUTHENTICODE**</dt> </dl> | Valor padrão. Especifica um carimbo de data/hora Authenticode.<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**\_Carimbo de data/hora do signatário \_ RFC3161**</dt> </dl>                | Especifica um carimbo de data/hora RFC 3161.<br/>                    |



 

Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* for **nulo**.

</dd> <dt>

*pszTimestampAlgorithmOid* \[ em, opcional\]
</dt> <dd>

Identificador de objeto do algoritmo a ser usado para criar um carimbo de data/hora RFC 3161. Esse parâmetro é ignorado para carimbos de data/hora Authenticode.

</dd> <dt>

*pwszHttpTimeStamp* \[ em, opcional\]
</dt> <dd>

URL do servidor de carimbo de data/hora.

</dd> <dt>

*psRequest* \[ em, opcional\]
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**\_ atributo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) -las que são adicionadas a uma solicitação de assinatura. Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* não contiver um valor válido ou for **NULL**.

</dd> <dt>

*pSipData* \[ em, opcional\]
</dt> <dd>

Um valor de 32 bits que é passado como dados adicionais para funções SIP. O formato e o conteúdo deste são definidos pelo provedor SIP.

</dd> <dt>

*ppSignerContext* \[ fora\]
</dt> <dd>

O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o [*blob*](../secgloss/b-gly.md)assinado. Quando você terminar de usar a estrutura de **\_ contexto do signatário** , libere a estrutura do **\_ contexto do signatário** chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ em, opcional\]
</dt> <dd>

Se presente, um ponteiro para uma estrutura de [**\_ \_ sinal \_ de segurança de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) que contém os parâmetros usados para verificar se há assinaturas fortes. Se um certificado ou sua cadeia não passar, o arquivo não será alterado de nenhuma forma. Se uma URL for passada para especificar uma autoridade de carimbo de data/hora (TSA), essa política também será aplicada ao carimbo de data/hora.

</dd> <dt>

*Preservação* 
</dt> <dd>

Reservado. Esse valor deve ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará S \_ OK.

Se a função falhar, ela retornará um valor **HRESULT** que indica o erro. Os códigos de erro possíveis retornados por essa função incluem, mas não se limitam a, o seguinte. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).



| Código de retorno                                                                                  | Descrição                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Se você definir o parâmetro *dwTimestampFlags* para o **assinante \_ timestamp \_ AUTHENTICODE**, não será possível definir o parâmetro *dwFlags* como **SIG \_ Append**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
