---
description: Computa a chave de segredo mestre do protocolo de protocolo SSL (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Função SslGenerateMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370794"
---
# <a name="sslgeneratemasterkey-function"></a>Função SslGenerateMasterKey

A função **SslGenerateMasterKey** computa a chave de segredo mestre do protocolo SSL ( [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
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

O identificador para a instância do provedor de protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ no\]
</dt> <dd>

O identificador para a [*chave privada*](/windows/desktop/SecGloss/p-gly) usada na troca.

</dd> <dt>

*hPublicKey* \[ no\]
</dt> <dd>

O identificador para a [*chave pública*](/windows/desktop/SecGloss/p-gly) usada na troca.

</dd> <dt>

*phMasterKey* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador para a [*chave mestra*](/windows/desktop/SecGloss/m-gly)gerada.

</dd> <dt>

*dwProtocol* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contém informações usadas como parte da operação de troca de chaves. O conjunto preciso de buffers depende do protocolo e do pacote de codificação usado. No mínimo, a lista conterá buffers que contêm os valores aleatórios de cliente e servidor fornecidos.

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

O endereço de um buffer que recebe o segredo mestre criptografado com a chave pública do servidor. O parâmetro *cbOutput* contém o tamanho desse buffer. Se esse parâmetro for **NULL**, essa função retornará o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .

> [!Note]  
> Esse buffer é usado ao executar uma troca de chaves RSA.

 

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ fora\]
</dt> <dd>

Um ponteiro para um valor **DWORD** no qual posicionar o número de bytes gravados no buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Especifica se essa função está sendo usada para troca de chaves do lado do cliente ou do servidor.



| Valor                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Sinalizador de cliente SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica uma troca de chaves do lado do cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Sinalizador de servidor SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica uma troca de chaves do lado do servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | Um dos identificadores fornecidos não é válido.<br/>                     |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phMasterKey* ou *hPublicKey* não é válido.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

