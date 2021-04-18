---
description: Recupera um identificador para o hash de handshake que é usado para autenticação de cliente.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Função SslCreateClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778696"
---
# <a name="sslcreateclientauthhash-function"></a>Função SslCreateClientAuthHash

A função **SslCreateClientAuthHash** recupera um identificador para o [*hash*](/windows/desktop/SecGloss/h-gly) de handshake que é usado para autenticação de cliente.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
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

Um ponteiro para uma variável de **\_ \_ identificador de hash NCRYPT** para receber o identificador de hash.

</dd> <dt>

*dwProtocol* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pszHashAlgId* \[ no\]
</dt> <dd>

Um dos valores de [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O parâmetro *hSslProvider* contém um ponteiro que não é válido.<br/>                |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phHandshakeHash* está definido como **NULL**.<br/>                               |
| <dl> <dt>**Nte \_ 0x80090029L sem \_ suporte**</dt> <dt></dt> </dl>     | A função selecionada não tem suporte na versão especificada da interface.<br/> |
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Memória insuficiente para alocar buffers.<br/>                                          |
| <dl> <dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt> </dl>         | O parâmetro *dwFlags* deve ser definido como zero.<br/>                                      |



 

## <a name="remarks"></a>Comentários

A função **SslCreateClientAuthHash** é chamada para o [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS 1,2 ou conversas posteriores para criar objetos hash que são usados para mensagens de handshake de hash. Ele é chamado uma vez para cada [*algoritmo de hash*](/windows/desktop/SecGloss/h-gly) possível que pode ser usado na assinatura de autenticação do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

