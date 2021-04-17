---
description: Importa uma chave para o provedor de protocolo de protocolo SSL protocolo (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Função SslImportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780481"
---
# <a name="sslimportkey-function"></a>Função SslImportKey

A função **SslImportKey** importa uma chave para o provedor de protocolo de [*protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo SSL.

</dd> <dt>

*phKey* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador da [*chave de criptografia*](/windows/desktop/SecGloss/c-gly) para receber a chave importada.

</dd> <dt>

*pszBlobType* \[ no\]
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que contém um identificador que especifica o tipo de [*blob*](/windows/desktop/SecGloss/b-gly) que está contido no buffer *pbInput* . Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ blob público do BCRYPT DH \_**</dt> </dl>    | Exportar uma [*chave pública*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman. O buffer *pbOutput* recebe uma estrutura de [**\_ \_ \_ blob de chave DH BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) imediatamente seguida pelos dados de chave.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BLOB de BCRYPT \_ ECCPUBLIC \_**</dt> </dl>     | Exportar uma [*chave pública*](/windows/desktop/SecGloss/p-gly)de [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC). O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ ECCKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) imediatamente seguida pelos dados de chave.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_blob de \_ chave \_ opaco de BCRYPT**</dt> </dl> | Exporte uma [*chave simétrica*](/windows/desktop/SecGloss/s-gly) em um formato específico para um único CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ). BLOBs opacos não são transferível e devem ser importados usando o mesmo CSP que gerou o BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BLOB de BCRYPT \_ RSAPUBLIC \_**</dt> </dl>     | Exportar uma chave pública [*RSA*](/windows/desktop/SecGloss/r-gly) . O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ RSAKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) imediatamente seguida pelos dados de chave.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ no\]
</dt> <dd>

Um ponteiro para o buffer que contém o [*blob de chave*](/windows/desktop/SecGloss/k-gly).

</dd> <dt>

*cbKeyBlob* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbKeyBlob* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O identificador *hSslProvider* não é válido.<br/>                       |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phKey* é **nulo**.<br/>                            |



 

## <a name="remarks"></a>Comentários

Você pode usar a função **SslImportKey** para importar chaves de sessão como parte do processo de transferência de chaves de sessão de um processo para outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

