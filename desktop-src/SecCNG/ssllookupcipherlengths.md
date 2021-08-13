---
description: Retorna uma \_ estrutura de \_ comprimentos de criptografia de SSL NCRYPT \_ que contém o cabeçalho e os comprimentos do trailer do protocolo de entrada, do conjunto de codificação e do tipo de chave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Função SslLookupCipherLengths (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3898b54946b9a1035ce8ec1fedabc218c750bff6579b39f195a1f60b378144f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905986"
---
# <a name="ssllookupcipherlengths-function"></a>Função SslLookupCipherLengths

A função **SslLookupCipherLengths** retorna uma estrutura de [**\_ \_ \_ comprimentos de criptografia de SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) que contém o cabeçalho e os comprimentos do trailer do protocolo de entrada, do conjunto de codificação e do tipo de chave.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
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

*pCipherLengths* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer para receber a estrutura de [**\_ \_ \_ comprimentos de criptografia de SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .

</dd> <dt>

*cbCipherLengths* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer apontado pelo parâmetro *pCipherLengths* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O parâmetro *hSslProvider* contém um ponteiro que não é válido.<br/>                                                      |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *pCipherLengths* está definido como **NULL** ou o comprimento do buffer especificado pelo *cbCipherLengths* é muito curto.<br/> |
| <dl> <dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt> </dl>         | O parâmetro *dwFlags* deve ser definido como zero.<br/>                                                                            |



 

## <a name="remarks"></a>Comentários

A função **SslLookupCipherLengths** é chamada para as conversas do [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS 1,1 ou posterior para consultar o cabeçalho e os comprimentos do trailer para o protocolo solicitado, o conjunto de codificação e o tipo de chave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

