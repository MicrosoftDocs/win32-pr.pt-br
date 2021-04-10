---
description: Time carimba o assunto especificado e dá suporte à configuração de carimbos de data/hora em várias assinaturas.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: Função SignerTimeStampEx3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089841"
---
# <a name="signertimestampex3-function"></a>Função SignerTimeStampEx3

O tempo da função **SignerTimeStampEx3** carimba o assunto especificado e dá suporte à definição de carimbos de data/hora em várias assinaturas.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
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

Sinalizador que especifica o tipo de carimbo de data/hora a ser gerado. Esse parâmetro pode usar um dos valores a seguir. Os valores são mutuamente exclusivos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </dl></td>
<td>Especifica um carimbo de data/hora Authenticode.<br/>
<blockquote>
[!Note]<br />
O Authenticode não é mais o tipo preferencial de carimbo de data/hora. O suporte para carimbos de data/hora Authenticode pode ser removido no futuro. É recomendável usar a RFC 3161 em vez disso.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </dl></td>
<td>Especifica um carimbo de data/hora compatível com RFC 3161.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*dwIndex* \[ no\]
</dt> <dd>

Especifica o número de sequência da assinatura à qual o carimbo de data/hora será adicionado. Se esse valor for zero (0), a assinatura externa estará com carimbo de data/hora.

</dd> <dt>

*pSubjectInfo* \[ no\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.

</dd> <dt>

*pwszHttpTimeStamp* \[ no\]
</dt> <dd>

O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.

</dd> <dt>

*pszAlgorithmOid* \[ no\]
</dt> <dd>

Um algoritmo de hash a ser usado para executar carimbos de data/hora compatíveis com o RFC 3161. Esse parâmetro é ignorado para carimbos de data/hora Authenticode.

</dd> <dt>

*psRequest* \[ em, opcional\]
</dt> <dd>

Opcional. O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.

Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.

</dd> <dt>

*pSipData* \[ em, opcional\]
</dt> <dd>

Opcional. Um valor de 32 bits que é passado como dados adicionais para funções de SIP ( [*pacote de interface de entidade*](../secgloss/s-gly.md) ). O formato e o conteúdo desse parâmetro são definidos pelo provedor SIP.

Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.

</dd> <dt>

*ppSignerContext* \[ fora\]
</dt> <dd>

Opcional. O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o blob assinado. Quando você terminar de usar a estrutura de **\_ contexto do assinante** , libere-a chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ em, opcional\]
</dt> <dd>

Se presente, um ponteiro para uma estrutura de [**\_ \_ sinal \_ de segurança de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) que contém os parâmetros usados para verificar se há assinaturas fortes. O carimbo de data/hora deve passar nesta política criptográfica.

</dd> <dt>

*Preservação* 
</dt> <dd>

Reservado. Esse valor deve ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará S \_ OK.

Se a função falhar, ela retornará um valor **HRESULT** que indica o erro. Os códigos de erro possíveis retornados por essa função incluem, mas não se limitam a, o seguinte. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Esse erro pode ser retornado para as seguintes condições:<br/>
<ul>
<li>Você deve definir <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> ou <strong>SIGNER_TIMESTAMP_RFC3161</strong> para o parâmetro <em>dwFlags</em> .</li>
<li>O parâmetro <em>preservado</em> deve ser <strong>nulo</strong>.</li>
<li>Se você definir o sinalizador <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> no parâmetro <em>dwFlags</em> , deverá definir o parâmetro <em>dwIndex</em> como zero.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
