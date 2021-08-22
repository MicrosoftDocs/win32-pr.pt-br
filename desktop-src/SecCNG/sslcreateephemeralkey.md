---
description: Cria uma chave efêmera para uso durante a autenticação que ocorre durante o handshake protocolo SSL protocolo SSL.
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Função SslCreateEphemeralKey (Sslprovider.h)
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
ms.openlocfilehash: a6a54de2865df805af51b054c22d455d52914a5b00514767d432ceda28c16a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907093"
---
# <a name="sslcreateephemeralkey-function"></a>Função SslCreateEphemeralKey

A **função SslCreateEphemeralKey** cria uma chave efêmera para uso durante [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) a autenticação que ocorre durante o handshake do protocolo SSL.

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle da instância do provedor de protocolo SSL.

</dd> <dt>

*phEphemeralKey* \[ out\]
</dt> <dd>

O alça da chave efêmera.

</dd> <dt>

*dwProtocol* \[ Em\]
</dt> <dd>

Um dos valores [**do Identificador de Protocolo do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Em\]
</dt> <dd>

Um dos valores do Identificador do Conjunto de Criptografia do Provedor [**SSL CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ Em\]
</dt> <dd>

Um dos valores do Identificador de Tipo de [**Chave do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) De definir esse parâmetro como zero [](/windows/desktop/SecGloss/e-gly) para tipos de chave que não são criptografia de curva elíptica (ECC).

</dd> <dt>

*dwKeyBitLen* \[ Em\]
</dt> <dd>

O comprimento, em bits, da chave.

</dd> <dt>

*pbParams* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer para conter parâmetros para a chave a ser criada. Se um conjunto de criptografias DHE (algoritmo de troca de [*chaves) Diffie-Hellman (efêmero)*](/windows/desktop/SecGloss/d-gly) não for usado, de definir o parâmetro *pbParams* como **NULL** e o parâmetro *cbParams* como zero.

</dd> <dt>

*cbParams* \[ Em\]
</dt> <dd>

O comprimento, em bytes, dos dados no buffer *pbParams.*

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.



| Valor/código de retorno                                                                                                                                                       | Descrição                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Não há memória suficiente para alocar o buffer.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | O *alça hSslProvider* não é válido.<br/>              |
| <dl> <dt>**NTE \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | Um dos parâmetros fornecidos não é válido.<br/>         |



 

## <a name="remarks"></a>Comentários

Ao usar um conjunto de criptografias DHE, a implementação SSL interna passa os parâmetros *de servidor p* e *g* para a função **SslCreateEphemeralKey** nos parâmetros *pbParams* e *cbParams.*

O formato dos dados no buffer *pbParams* é o mesmo usado ao definir a propriedade [**BCRYPT \_ DH \_ PARAMETERS**](cng-property-identifiers.md) e começa com uma estrutura [**BCRYPT \_ DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

