---
description: Time carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de contexto de signatário \_ que contém um ponteiro para um blob.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: Função SignerTimeStampEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662912"
---
# <a name="signertimestampex-function"></a>Função SignerTimeStampEx

O tempo da função **SignerTimeStampEx** carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de [**\_ contexto de signatário**](signer-context.md) que contém um ponteiro para um [*blob*](../secgloss/b-gly.md). Essa função dá suporte a carimbo de data/hora de Authenticode. Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado. Esse parâmetro deve ser definido como zero.

</dd> <dt>

*pSubjectInfo* \[ no\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.

</dd> <dt>

*pwszHttpTimeStamp* \[ no\]
</dt> <dd>

O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> </dl>

 

 
