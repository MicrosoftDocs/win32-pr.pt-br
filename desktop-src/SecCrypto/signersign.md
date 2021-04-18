---
description: Assina o arquivo especificado.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Função SignerSign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788100"
---
# <a name="signersign-function"></a>Função SignerSign

A função **SignerSign** assina o arquivo especificado.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

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

Um ponteiro para uma estrutura de [**\_ \_ informações do provedor de assinante**](signer-provider-info.md) que especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de [*chave privada*](../secgloss/p-gly.md) usadas para criar a assinatura digital.

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

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará S \_ OK.

Se a função falhar, ela retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
