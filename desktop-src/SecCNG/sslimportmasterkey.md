---
description: Executa uma operação de troca de protocolo SSL protocolo SSL.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Função SslImportMasterKey (Sslprovider.h)
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
ms.openlocfilehash: 546cfeb39ac413b99b5b8021dc7dd6f0f57a89dbfb87880a63b0db2324cda0d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906057"
---
# <a name="sslimportmasterkey-function"></a>Função SslImportMasterKey

A **função SslImportMaster** [*protocolo SSL Key*](/windows/desktop/SecGloss/s-gly) executa uma operação de troca de chaves SSL (protocolo S) do lado do servidor.

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle para a instância do provedor de protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ Em\]
</dt> <dd>

O alça para a [*chave privada*](/windows/desktop/SecGloss/p-gly) usada na troca.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Um ponteiro para o handle para receber a [*chave mestra*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ Em\]
</dt> <dd>

Um dos valores [**do Identificador de Protocolo do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Em\]
</dt> <dd>

Um dos valores de Identificadores do Pacote de [**Criptografia do Provedor SSL CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ Em\]
</dt> <dd>

Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contêm informações usadas como parte da operação de troca de chaves. O conjunto preciso de buffers depende do protocolo e do conjunto de criptografia que é usado. No mínimo, a lista conterá buffers que contêm os valores aleatórios fornecidos pelo cliente e pelo servidor.

</dd> <dt>

*pbEncryptedKey* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer que contém a chave secreta pré-mestre criptografada criptografada com a [*chave pública*](/windows/desktop/SecGloss/p-gly) do servidor.

</dd> <dt>

*cbEncryptedKey* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do *buffer pbEncryptedKey.*

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Defina esse parâmetro como **NCRYPT \_ SSL \_ SERVER \_ FLAG** para indicar que esta é uma chamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Não há memória suficiente disponível para alocar buffers necessários.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Um dos alças fornecidos não é válido.<br/>                     |
| <dl> <dt>**NTE \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | O *parâmetro phMasterKey* é **NULL.**<br/>                      |



 

## <a name="remarks"></a>Comentários

Essa função descriptografa o segredo do pré-mestre, calcula o segredo mestre SSL e retorna um identificador para esse objeto para o chamador. Essa chave mestra pode ser usada para derivar a chave de sessão SSL e concluir o handshake SSL.

> [!Note]  
> Essa função é usada quando o algoritmo de troca de chaves [*RSA*](/windows/desktop/SecGloss/r-gly) está sendo usado. Quando [*o DH*](/windows/desktop/SecGloss/d-gly) é usado, o código do servidor chama [**SslGenerateMasterKey.**](sslgeneratemasterkey.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

