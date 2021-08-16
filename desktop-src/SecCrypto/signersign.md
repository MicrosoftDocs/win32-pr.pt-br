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
ms.openlocfilehash: d9756fba3a931ddf09715b5086e613a9395c10c57c82fa18c64007aeb02b615c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973130"
---
# <a name="signersign-function"></a>Função SignerSign

A **função SignerSign** assina o arquivo especificado.

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

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

*pSubjectInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que especifica o assunto a ser assinar.

</dd> <dt>

*pSignerCert* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ SIGNER CERT**](signer-cert.md) que especifica o certificado a ser usado para criar a assinatura digital.

</dd> <dt>

*pSignatureInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**DE INFORMAÇÕES DE ASSINATURA \_ \_ DO SIGNER**](signer-signature-info.md) que contém informações sobre a assinatura digital.

</dd> <dt>

*pProviderInfo* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) que especifica o CSP [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia) e as informações de chave [*privada*](../secgloss/p-gly.md) usadas para criar a assinatura digital.

Se o valor desse parâmetro for **NULL,** o valor do parâmetro *pSignerCert* deverá especificar um certificado associado a um CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, opcional\]
</dt> <dd>

A URL de um servidor de carimbo de data/hora.

</dd> <dt>

*psRequest* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma matriz de [**estruturas CRYPT \_ ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que são adicionadas a uma solicitação de sinalização. Esse parâmetro será ignorado se *o parâmetro pwszHttpTimeStamp* não tiver um valor válido que não seja **NULL.**

</dd> <dt>

*pSipData* \[ in, opcional\]
</dt> <dd>

Um valor de 32 bits que é passado como dados adicionais para funções SIP. O formato e o conteúdo disso são definidos pelo provedor SIP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará S \_ OK.

Se a função falhar, ela retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
