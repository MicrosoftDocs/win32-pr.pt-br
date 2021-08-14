---
description: 'Retorna o identificador de algoritmo da API de criptografia: próxima geração (CNG) do algoritmo de hash que é usado para a função pseudo aleatória (TLS) do protocolo de segurança da camada de transporte (PRF) para o protocolo de entrada, o conjunto de codificação e o tipo de chave.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Função SslGetCipherSuitePRFHashAlgorithm (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: f328f5e4746d3a66f614e8ccbbfe66bbf3475b7f7a1a98a8a68c11df96412bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906158"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>Função SslGetCipherSuitePRFHashAlgorithm

A função **SslGetCipherSuitePRFHashAlgorithm** retorna o identificador de algoritmo CNG (Cryptography API: Next Generation) do [*algoritmo de hash*](/windows/desktop/SecGloss/h-gly) que é usado para a [*função pseudo-aleatória*](/windows/desktop/SecGloss/p-gly) do [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS para o protocolo de entrada, o conjunto de codificação e o tipo de chave.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

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

Um dos valores do [**identificador do tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Para tipos de chave que não são ECC ( [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) ), defina esse parâmetro como zero.

</dd> <dt>

*szPRFHash* \[ fora\]
</dt> <dd>

Um dos [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) para o hash que será usado para o TLS PRF.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O parâmetro *hSslProvider* contém um ponteiro que não é válido.<br/>                |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *szPRFHash* está definido como **NULL**.<br/>                                     |
| <dl> <dt>**Nte \_ 0x80090029L sem \_ suporte**</dt> <dt></dt> </dl>     | A função selecionada não tem suporte na versão especificada da interface.<br/> |
| <dl> <dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt> </dl>         | O parâmetro *dwFlags* deve ser definido como zero.<br/>                                      |



 

## <a name="remarks"></a>Comentários

Essa função **SslGetCipherSuitePRFHashAlgorithm** é chamada para conversações TLS 1,2 ou posteriores para consultar o algoritmo de hash que será usado no TLS PRF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

