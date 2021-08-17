---
description: Calcula o hash enviado na mensagem concluída do handshake protocolo SSL protocolo SSL.
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Função SslComputeFinishedHash (Sslprovider.h)
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
ms.openlocfilehash: e0f23a58111bfcebbe668cd3b6c50a135da0dae240907f09a65d60ef1cebdda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907137"
---
# <a name="sslcomputefinishedhash-function"></a>Função SslComputeFinishedHash

A **função SslComputeFinishedHash** calcula o hash enviado na mensagem concluída do [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) [*handshake*](/windows/desktop/SecGloss/h-gly) do protocolo SSL. Para obter mais informações sobre a sequência de handshake SSL, consulte Descrição do [handshake protocolo SSL (SSL).](https://support.microsoft.com/kb/257591)

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle da instância do provedor de protocolo SSL.

</dd> <dt>

*hMasterKey* \[ Em\]
</dt> <dd>

O identificador do [*objeto de chave*](/windows/desktop/SecGloss/m-gly) mestra.

</dd> <dt>

*hHandshakeHash* \[ Em\]
</dt> <dd>

O handle do hash das mensagens de handshake.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o hash para a mensagem de finalização.

</dd> <dt>

*cbOutput* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do *buffer pbOutput.*

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Uma das constantes a seguir.



| Valor                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ Sinalizador DE \_ \_ CLIENTE SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica que essa é uma chamada de cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ Sinalizador DE \_ \_ SERVIDOR SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica que essa é uma chamada de servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.



| Valor/código de retorno                                                                                                                                                                | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ 2148073510 \_ DE**</dt> <dt>2148073510 INVÁLIDO (0x80090026)</dt> </dl> | Um dos alças fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

A **função SslComputeFinishedHash** é uma das três funções usadas para gerar um hash a ser usado durante o handshake SSL.

1.  A [**função SslCreateHandshakeHash**](sslcreatehandshakehash.md) é chamada para obter um alça de hash.
2.  A [**função SslHashHandshake**](sslhashhandshake.md) é chamada de qualquer número de vezes com o alça de hash para adicionar dados ao hash.
3.  A **função SslComputeFinishedHash** é chamada com o alça de hash para obter o resumo dos dados com hash.

O valor de hash é calculado com hash do segredo mestre com um hash de todas as mensagens de handshake enviadas ou recebidas anteriores.

O valor de *cbOutput* determina o comprimento dos dados de hash. Quando o [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS 1.0 é usado, isso sempre deve ser 12 (bytes). Para obter mais informações, [consulte O protocolo TLS versão 1.0](https://www.ietf.org/rfc/rfc2246.txt).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

