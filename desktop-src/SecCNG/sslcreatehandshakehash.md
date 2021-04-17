---
description: Obtém um identificador de hash que é usado para mensagens de handshake de hash.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Função SslCreateHandshakeHash (Sslprovider. h)
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
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770354"
---
# <a name="sslcreatehandshakehash-function"></a>Função SslCreateHandshakeHash

A função **SslCreateHandshakeHash** Obtém um identificador de hash que é usado para mensagens de handshake de hash.

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

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phHandshakeHash* \[ fora\]
</dt> <dd>

Um identificador de hash que pode ser passado para outras funções de provedor de SSL.

</dd> <dt>

*dwProtocol* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

> [!Note]  
> Essa função não é usada com o protocolo SSL 2,0.

 

</dd> <dt>

*dwCipherSuite* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Memória insuficiente para alocar o buffer de hash.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O identificador *hSslProvider* não é válido.<br/>                   |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O *phHandshakeHash* é nulo.<br/>                            |



 

## <a name="remarks"></a>Comentários

A função **SslCreateHandshakeHash** é uma das três funções usadas para gerar um hash a ser usado durante o HANDSHAKE de SSL.

1.  A função **SslCreateHandshakeHash** é chamada para obter um identificador de hash.
2.  A função [**SslHashHandshake**](sslhashhandshake.md) é chamada qualquer número de vezes com o identificador de hash para adicionar dados ao hash.
3.  A função [**SslComputeFinishedHash**](sslcomputefinishedhash.md) é chamada com o identificador de hash para obter o resumo dos dados com hash.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

