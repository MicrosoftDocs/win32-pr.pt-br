---
description: Carimbos de data/hora do assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura SIGNER CONTEXT que contém um \_ ponteiro para um BLOB. Essa função pode ser usada para executar a Infraestrutura de Chave Pública X.509, RFC 3161&\# 8211;em conformidade, carimbos de data/hora.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: Função SignerTimeStampEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c5a9bfc81c3196657f611c9263e0d957ca867a64479b34900dce7078237e195f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898265"
---
# <a name="signertimestampex2-function"></a>Função SignerTimeStampEx2

A **função SignerTimeStampEx2** marca o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura [**SIGNER \_ CONTEXT**](signer-context.md) que contém um ponteiro para um [*BLOB*](../secgloss/b-gly.md). Essa função pode ser usada para executar a Infraestrutura de Chave Pública X.509, carimbos de data/hora compatíveis com RFC 3161.

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Valor que especifica o tipo de carimbo de data/hora a ser gerado. Esse parâmetro pode usar um dos valores a seguir. Os valores são mutuamente exclusivos.



| Valor                                                                                                                                                                                                          | Significado                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**\_AUTHENTICODE DO SIGNER TIMESTAMP \_**</dt> </dl> | Especifica um carimbo de data/hora authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**SIGNER \_ TIMESTAMP \_ RFC3161**</dt> </dl>                | Especifica um carimbo de data/hora compatível com RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ Em\]
</dt> <dd>

O endereço de uma estrutura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que representa o assunto a ser marcado por hora.

</dd> <dt>

*pwszHttpTimeStamp* \[ Em\]
</dt> <dd>

O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.

</dd> <dt>

*dwAlgId* \[ Em\]
</dt> <dd>

Especifica um algoritmo de hash a ser usado para executar carimbos de data/hora compatíveis com RFC 3161. Esse parâmetro é ignorado para carimbos de data/hora authenticode.

</dd> <dt>

*psRequest* \[ Em\]
</dt> <dd>

Opcional. O endereço de uma estrutura [**CRYPT \_ ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.

Esse parâmetro é opcional e pode ser **NULL** se não estiver incluído.

</dd> <dt>

*pSipData* \[ Em\]
</dt> <dd>

Opcional. Um valor de 32 bits que é passado como dados adicionais para funções SIP [*(pacote de interface*](../secgloss/s-gly.md) de assunto). O formato e o conteúdo desse parâmetro são definidos pelo provedor SIP.

Esse parâmetro é opcional e pode ser **NULL** se não estiver incluído.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Opcional. O endereço de um ponteiro para a estrutura [**SIGNER \_ CONTEXT**](signer-context.md) que contém o BLOB assinado. Quando terminar de usar a estrutura **SIGNER \_ CONTEXT,** livre-a chamando a [**função SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará S \_ OK.

Se a função falhar, ela retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
