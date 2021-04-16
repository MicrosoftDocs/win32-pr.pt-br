---
description: Executa uma operação de troca de chaves do protocolo SSL (protocolo SSL do servidor).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Função SslImportMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750500"
---
# <a name="sslimportmasterkey-function"></a>Função SslImportMasterKey

A função **SslImportMasterKey** executa uma operação de troca de chaves de protocolo SSL ( [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) do servidor).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
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

*phMasterKey* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador para receber a [*chave mestra*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ no\]
</dt> <dd>

Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ no\]
</dt> <dd>

Um dos valores dos [**identificadores do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contém informações usadas como parte da operação de troca de chaves. O conjunto preciso de buffers depende do protocolo e do pacote de codificação usado. No mínimo, a lista conterá buffers que contêm os valores aleatórios de cliente e servidor fornecidos.

</dd> <dt>

*pbEncryptedKey* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém a chave secreta criptografada do mestre criptografada com a [*chave pública*](/windows/desktop/SecGloss/p-gly) do servidor.

</dd> <dt>

*cbEncryptedKey* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbEncryptedKey* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Defina esse parâmetro como **o \_ \_ \_ sinalizador de servidor SSL NCRYPT** para indicar que esta é uma chamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | Um dos identificadores fornecidos não é válido.<br/>                     |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phMasterKey* é **nulo**.<br/>                      |



 

## <a name="remarks"></a>Comentários

Essa função descriptografa o segredo de mestre, computa o segredo mestre do SSL e retorna um identificador para esse objeto para o chamador. Essa chave mestra pode então ser usada para derivar a chave de sessão SSL e concluir o handshake de SSL.

> [!Note]  
> Essa função é usada quando o algoritmo de troca de chave [*RSA*](/windows/desktop/SecGloss/r-gly) está sendo usado. Quando [*DH*](/windows/desktop/SecGloss/d-gly) é usado, o código do servidor chama [**SslGenerateMasterKey**](sslgeneratemasterkey.md) em vez disso.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

