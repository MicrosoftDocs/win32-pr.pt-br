---
description: Computa o hash enviado na mensagem concluída do handshake do protocolo de protocolo SSL (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Função SslComputeFinishedHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921414"
---
# <a name="sslcomputefinishedhash-function"></a>Função SslComputeFinishedHash

A função **SslComputeFinishedHash** computa o [*hash*](/windows/desktop/SecGloss/h-gly) enviado na mensagem concluída do handshake do [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL). Para obter mais informações sobre a sequência de handshake SSL, consulte [Descrição do handshake de protocolo SSL (SSL)](https://support.microsoft.com/kb/257591).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo SSL.

</dd> <dt>

*hMasterKey* \[ no\]
</dt> <dd>

O identificador do objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ no\]
</dt> <dd>

O identificador do hash das mensagens de handshake.

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o hash da mensagem de conclusão.

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Uma das constantes a seguir.



| Valor                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Sinalizador de cliente SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica que esta é uma chamada de cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Sinalizador de servidor SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica que esta é uma chamada de servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.



| Código/valor de retorno                                                                                                                                                                | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>2148073510 (0x80090026)</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

A função **SslComputeFinishedHash** é uma das três funções usadas para gerar um hash a ser usado durante o HANDSHAKE de SSL.

1.  A função [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) é chamada para obter um identificador de hash.
2.  A função [**SslHashHandshake**](sslhashhandshake.md) é chamada qualquer número de vezes com o identificador de hash para adicionar dados ao hash.
3.  A função **SslComputeFinishedHash** é chamada com o identificador de hash para obter o resumo dos dados com hash.

O valor de hash é computado pelo hash do segredo mestre com um hash de todas as mensagens de handshake anteriores enviadas ou recebidas.

O valor de *cbOutput* determina o comprimento dos dados de hash. Quando o protocolo TLS 1,0 é usado [*, ele deve*](/windows/desktop/SecGloss/t-gly) ser sempre 12 (bytes). Para obter mais informações, consulte [o protocolo TLS versão 1,0](https://www.ietf.org/rfc/rfc2246.txt).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

