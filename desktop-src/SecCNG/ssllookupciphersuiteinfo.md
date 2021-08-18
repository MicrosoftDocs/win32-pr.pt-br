---
description: Recupera as informações do conjunto de criptografias para um protocolo, conjunto de criptografias e conjunto de tipos de chave especificados.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Função SslLookupCipherSuiteInfo (Sslprovider.h)
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
ms.openlocfilehash: bf56f199ae0d367517558a12a0e84bf8ce26e7bdf5f70625b878066152d0b696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905605"
---
# <a name="ssllookupciphersuiteinfo-function"></a>Função SslLookupCipherSuiteInfo

A **função SslLookupCipherSuiteInfo** recupera as informações do conjunto de criptografias para um protocolo, conjunto de criptografias e conjunto de tipos de chave especificados.

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle para a [*instância do provedor protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) SSL.

</dd> <dt>

*dwProtocol* \[ Em\]
</dt> <dd>

Um dos valores [**do Identificador de Protocolo do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Em\]
</dt> <dd>

Um dos valores de Identificadores do Pacote de [**Criptografia do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ Em\]
</dt> <dd>

Um dos valores de Identificadores de Tipo de Chave do Provedor [**SSL CNG.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx)

</dd> <dt>

*pCipherSuite* \[ out\]
</dt> <dd>

O endereço de um buffer que contém uma estrutura [**NCRYPT \_ SSL \_ CIPHER \_ SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) na qual gravar as informações do conjunto de criptografias.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                    | Descrição                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | O *alça hSslProvider* não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

