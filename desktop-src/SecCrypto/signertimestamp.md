---
description: A hora carimba o assunto especificado. Essa função dá suporte a carimbo de data/hora de Authenticode. Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Função SignerTimeStamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: cb33852cb2860a29d43a41b2331a910a098384b872e972a74cf94f627bebf75a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898292"
---
# <a name="signertimestamp-function"></a>Função SignerTimeStamp

O tempo da função **SignerTimeStamp** carimba o assunto especificado. Essa função dá suporte a carimbo de data/hora de Authenticode. Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSubjectInfo* \[ no\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.

</dd> <dt>

*pwszHttpTimeStamp* \[ no\]
</dt> <dd>

O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.

</dd> <dt>

*psRequest* \[ em, opcional\]
</dt> <dd>

O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.

Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.

</dd> <dt>

*pSipData* \[ em, opcional\]
</dt> <dd>

Um valor de 32 bits que é passado como dados adicionais para funções SIP. O formato e o conteúdo deste são definidos pelo provedor SIP.

Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.

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



 

 
