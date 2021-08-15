---
description: Assina o arquivo especificado e retorna um ponteiro para os dados assinados.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Função SignerSignEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 0b880cc02053d5a90089cffc721b057c6fce9f34b8be6517c12ef59fef9e0ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898319"
---
# <a name="signersignex-function"></a>Função SignerSignEx

A função **SignerSignEx** assina o arquivo especificado e retorna um ponteiro para os dados assinados.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Modifica o comportamento dessa função.

Se o arquivo a ser assinado for um arquivo executável portátil (PE), isso poderá ser zero ou uma combinação de um ou mais dos valores a seguir. Esses identificadores são definidos em Mssip. h.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_ \_ \_ \_ Sinalizador de hashes de página do PE do exc**</dt> <dt></dt> </dl>                    | Exclua os hashes de página ao criar dados indiretos SIP para o arquivo PE. Esse sinalizador tem precedência sobre o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** .<br/> Se nem o sinalizador de **\_ \_ \_ \_ hashes \_ de página do SPC exc PE** ou o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** . do SPC for especificado, o valor definido com a função [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) será usado para essa configuração. O padrão para essa configuração é excluir hashes de página ao criar dados indiretos SIP para arquivos PE.<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ \_Sinalizador de \_ \_ tabela de \_ \_ end de importação do PE Inc**</dt> <dt></dt> </dl> | Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ 0x40 \_ do \_ \_ \_ sinalizador de informações de depuração Inc PE**</dt> <dt></dt> </dl>                       | Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ 0x80 \_ de \_ \_ sinalizador de recursos do PE Inc**</dt> <dt></dt> </dl>                           | Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ 0x100 \_ do \_ \_ \_ sinalizador de hash da página do PE Inc**</dt> <dt></dt> </dl>                   | Inclua hashes de página ao criar dados indiretos SIP para o arquivo PE.<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pSubjectInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que especifica o assunto a ser assinado.

</dd> <dt>

*pSignerCert* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ certificado de signatário**](signer-cert.md) que especifica o certificado a ser usado para criar a assinatura digital.

</dd> <dt>

*pSignatureInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de assinatura de assinante**](signer-signature-info.md) que contém informações sobre a assinatura digital.

</dd> <dt>

*pProviderInfo* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações do provedor de assinante**](signer-provider-info.md) que especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de chave privada usadas para criar a assinatura digital.

Se o valor desse parâmetro for **nulo**, o valor do parâmetro *pSignerCert* deverá especificar um certificado associado a um CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ em, opcional\]
</dt> <dd>

A URL de um servidor de carimbo de data/hora.

</dd> <dt>

*psRequest* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma matriz de estruturas de [**\_ atributo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) -las que são adicionadas a uma solicitação de assinatura. Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* não contiver um valor válido que não seja **nulo**.

</dd> <dt>

*pSipData* \[ em, opcional\]
</dt> <dd>

Um valor de 32 bits que é passado como dados adicionais para funções SIP. O formato e o conteúdo deste são definidos pelo provedor SIP.

</dd> <dt>

*ppSignerContext* \[ fora\]
</dt> <dd>

O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o [*blob*](../secgloss/b-gly.md)assinado. Quando você terminar de usar a estrutura de **\_ contexto do signatário** , libere a estrutura do **\_ contexto do signatário** chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, a função retornará S \_ OK.

Se a função falhar, ela retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
