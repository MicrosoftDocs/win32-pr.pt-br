---
description: Time carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de contexto de signatário \_ que contém um ponteiro para um blob. Essa função pode ser usada para executar a infraestrutura de chave pública X. 509, RFC 3161&\# 8211; em conformidade, carimbos de data/hora.
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
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769269"
---
# <a name="signertimestampex2-function"></a>Função SignerTimeStampEx2

O tempo da função **SignerTimeStampEx2** carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de [**\_ contexto de signatário**](signer-context.md) que contém um ponteiro para um [*blob*](../secgloss/b-gly.md). Essa função pode ser usada para executar a infraestrutura de chave pública X. 509, em conformidade com a RFC 3161 – carimbos de data/hora.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

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

*dwFlags* \[ no\]
</dt> <dd>

Valor que especifica o tipo de carimbo de data/hora a ser gerado. Esse parâmetro pode usar um dos valores a seguir. Os valores são mutuamente exclusivos.



| Valor                                                                                                                                                                                                          | Significado                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**\_carimbo de data/hora do signatário \_ AUTHENTICODE**</dt> </dl> | Especifica um carimbo de data/hora Authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**\_Carimbo de data/hora do signatário \_ RFC3161**</dt> </dl>                | Especifica um carimbo de data/hora compatível com RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ no\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.

</dd> <dt>

*pwszHttpTimeStamp* \[ no\]
</dt> <dd>

O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.

</dd> <dt>

*dwAlgId* \[ no\]
</dt> <dd>

Especifica um algoritmo de hash a ser usado para executar carimbos de data/hora compatíveis com RFC 3161. Esse parâmetro é ignorado para carimbos de data/hora Authenticode.

</dd> <dt>

*psRequest* \[ no\]
</dt> <dd>

Opcional. O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.

Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.

</dd> <dt>

*pSipData* \[ no\]
</dt> <dd>

Opcional. Um valor de 32 bits que é passado como dados adicionais para funções de SIP ( [*pacote de interface de entidade*](../secgloss/s-gly.md) ). O formato e o conteúdo desse parâmetro são definidos pelo provedor SIP.

Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.

</dd> <dt>

*ppSignerContext* \[ fora\]
</dt> <dd>

Opcional. O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o blob assinado. Quando você terminar de usar a estrutura de **\_ contexto do assinante** , libere-a chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará S \_ OK.

Se a função falhar, ela retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
