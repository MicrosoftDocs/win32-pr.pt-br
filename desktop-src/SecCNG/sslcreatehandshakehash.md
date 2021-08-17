---
description: Obtém um alça de hash usado para mensagens de handshake de hash.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Função SslCreateHandshakeHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ea481a5b577c41eafddf9db8d80b4a3a1fe42d801bf96ed8cbc57127a4a8d91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906823"
---
# <a name="sslcreatehandshakehash-function"></a>Função SslCreateHandshakeHash

A **função SslCreateHandshakeHash** obtém um alça de hash usado para mensagens de handshake de hash.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ Em\]
</dt> <dd>

O handle da instância [*do provedor protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) SSL.

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Um alça de hash que pode ser passado para outras funções do provedor SSL.

</dd> <dt>

*dwProtocol* \[ Em\]
</dt> <dd>

Um dos valores [**do Identificador de Protocolo do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

> [!Note]  
> Essa função não é usada com o protocolo SSL 2.0.

 

</dd> <dt>

*dwCipherSuite* \[ Em\]
</dt> <dd>

Um dos valores do Identificador do Conjunto de Criptografia do Provedor [**SSL CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                       | Descrição                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Não há memória suficiente para alocar o buffer de hash.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | O *alça hSslProvider* não é válido.<br/>                   |
| <dl> <dt>**NTE \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | A *phHandshakeHash* é nula.<br/>                            |



 

## <a name="remarks"></a>Comentários

A **função SslCreateHandshakeHash** é uma das três funções usadas para gerar um hash a ser usado durante o handshake SSL.

1.  A **função SslCreateHandshakeHash** é chamada para obter um alça de hash.
2.  A [**função SslHashHandshake**](sslhashhandshake.md) é chamada de qualquer número de vezes com o alça de hash para adicionar dados ao hash.
3.  A [**função SslComputeFinishedHash**](sslcomputefinishedhash.md) é chamada com o alça de hash para obter o resumo dos dados com hash.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

