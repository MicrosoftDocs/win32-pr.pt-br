---
description: Enumera os conjuntos de codificação com suporte de um provedor de protocolo SSL (protocolo SSL Protocol).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Função SslEnumCipherSuites (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7d9fb40bf6bfebff6d0659640dfb68b718586ac822c8a779a56de300b8d55b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906688"
---
# <a name="sslenumciphersuites-function"></a>Função SslEnumCipherSuites

A função **SslEnumCipherSuites** enumera os conjuntos de codificação com suporte de um provedor de protocolo SSL ( [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ em, opcional\]
</dt> <dd>

O identificador de uma [*chave privada*](/windows/desktop/SecGloss/p-gly). Quando uma chave privada é especificada, o **SslEnumCipherSuites** enumera os conjuntos de codificação que são compatíveis com a chave privada. Por exemplo, se a chave privada for uma chave DSS, somente os pacotes de \_ codificação DSS DHE serão retornados. Se a chave privada for uma chave RSA, mas não der suporte a operações de descriptografia brutas, os conjuntos de codificação SSL2 não serão retornados.

Defina esse parâmetro como **NULL** quando você não estiver especificando uma chave privada.

> [!Note]  
> Um identificador *hPrivateKey* é obtido chamando a função [**SslOpenPrivateKey**](sslopenprivatekey.md) . Não há suporte para identificadores obtidos da função [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .

 

</dd> <dt>

*ppCipherSuite* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**NCRYPT do \_ \_ \_ pacote de criptografia SSL**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) para receber o endereço do próximo conjunto de codificação na lista.

</dd> <dt>

*ppEnumState* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um buffer que indica a posição atual na lista de conjuntos de codificação.

Defina o ponteiro como **nulo** na primeira chamada para **SslEnumCipherSuites**. Em cada chamada subsequente, passe o valor não modificado de volta para **SslEnumCipherSuites**.

Quando não houver mais conjuntos de codificação disponíveis, você deverá liberar *ppEnumState* chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Descrição                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>      | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/>                     |
| <dl> <dt>**Nte \_ Não há \_ mais \_ itens**</dt> <dt>0x8009002AL</dt> </dl> | Não há suporte para conjuntos de codificação adicionais.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para enumerar todos os conjuntos de codificação com suporte pelo provedor SSL, chame a função **SslEnumCipherSuites** em um loop até que o **nte não seja retornado \_ \_ mais \_ itens** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>NCrypt. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_pacote de \_ codificação \_ SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

