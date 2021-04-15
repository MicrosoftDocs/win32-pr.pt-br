---
description: Cria uma chave efêmera para uso durante a autenticação que ocorre durante o handshake do protocolo de protocolo SSL (SSL).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Função SslCreateEphemeralKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747647"
---
# <a name="sslcreateephemeralkey-function"></a>Função SslCreateEphemeralKey

A função **SslCreateEphemeralKey** cria uma chave efêmera para uso durante a autenticação que ocorre durante o handshake do [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo SSL.

</dd> <dt>

*phEphemeralKey* \[ fora\]
</dt> <dd>

O identificador da chave efêmera.

</dd> <dt>

*dwProtocol* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwKeyType* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Defina esse parâmetro como zero para os tipos de chave que não são ECC ( [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) ).

</dd> <dt>

*dwKeyBitLen* \[ no\]
</dt> <dd>

O comprimento, em bits, da chave.

</dd> <dt>

*pbParams* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém parâmetros para a chave a ser criada. Se um conjunto de codificação de DHE [*(algoritmo de troca de chaves) Diffie-Hellman (efêmero)*](/windows/desktop/SecGloss/d-gly) não for usado, defina o parâmetro *pbParams* como **nulo** e o parâmetro *cbParams* como zero.

</dd> <dt>

*cbParams* \[ no\]
</dt> <dd>

O comprimento, em bytes, dos dados no buffer *pbParams* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Memória insuficiente para alocar o buffer.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O identificador *hSslProvider* não é válido.<br/>              |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | Um dos parâmetros fornecidos não é válido.<br/>         |



 

## <a name="remarks"></a>Comentários

Ao usar um DHE Cipher Suite, a implementação SSL interna passa os parâmetros *p* e *g* do servidor para a função **SslCreateEphemeralKey** nos parâmetros *pbParams* e *cbParams* .

O formato dos dados no buffer *pbParams* é o mesmo usado ao definir a propriedade de parâmetros de [**\_ DH BCrypt \_**](cng-property-identifiers.md) e começa com uma estrutura de cabeçalho de [**\_ parâmetro BCrypt \_ DH \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

