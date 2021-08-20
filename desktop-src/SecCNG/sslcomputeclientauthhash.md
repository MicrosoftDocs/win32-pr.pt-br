---
description: Computa um hash a ser usado durante a autenticação do certificado.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Função SslComputeClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 59d1a4d8491175acb0f833cbafb430faae9b36b38a179970b7a99d6b0077591d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907157"
---
# <a name="sslcomputeclientauthhash-function"></a>Função SslComputeClientAuthHash

A função **SslComputeClientAuthHash** computa um [*hash*](/windows/desktop/SecGloss/h-gly) a ser usado durante a autenticação do [*certificado*](/windows/desktop/SecGloss/c-gly) .

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hMasterKey* \[ no\]
</dt> <dd>

O identificador do objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ no\]
</dt> <dd>

O identificador do hash do handshake calculado até o momento.

</dd> <dt>

*pszAlgId* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que identifica o [*algoritmo criptográfico*](/windows/desktop/SecGloss/c-gly)solicitado. Pode ser um dos [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) padrão ou o identificador para outro algoritmo registrado.

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

O endereço de um buffer que recebe o [*blob de chave*](/windows/desktop/SecGloss/k-gly). O parâmetro *cbOutput* contém o tamanho desse buffer. Se esse parâmetro for **NULL**, essa função coloca o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ fora\]
</dt> <dd>

Um ponteiro para um valor **DWORD** que especifica o comprimento, em bytes, do hash gravado no buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

A função **SslComputeClientAuthHash** computa o hash que é enviado na mensagem de verificação de certificado do handshake SSL. O valor de hash é calculado com a criação de um hash que contém o segredo mestre com um hash de todas as mensagens de handshake anteriores enviadas ou recebidas. Para obter mais informações sobre a sequência de handshake SSL, consulte [Descrição do handshake de protocolo SSL (SSL)](https://support.microsoft.com/kb/257591).

A maneira como o hash é calculado depende do protocolo e do conjunto de codificação usado. Além disso, o hash depende do tipo de chave de autenticação de cliente usada; o parâmetro *pszAlgId* indica o tipo de chave usada para autenticação de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

