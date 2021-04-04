---
description: Recupera as informações do pacote de codificação para um protocolo especificado, um conjunto de codificação e um conjunto de tipos de chave.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Função SslLookupCipherSuiteInfo (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837388"
---
# <a name="ssllookupciphersuiteinfo-function"></a>Função SslLookupCipherSuiteInfo

A função **SslLookupCipherSuiteInfo** recupera as informações do pacote de codificação para um protocolo especificado, o conjunto de codificação e o conjunto de tipos de chave.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*dwProtocol* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ no\]
</dt> <dd>

Um dos valores dos [**identificadores do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwKeyType* \[ no\]
</dt> <dd>

Um dos valores dos [**identificadores de tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .

</dd> <dt>

*pCipherSuite* \[ fora\]
</dt> <dd>

O endereço de um buffer que contém uma estrutura de [**\_ pacote de \_ criptografia \_ de SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) na qual gravar as informações do pacote de codificação.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Description                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | O identificador *hSslProvider* não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

