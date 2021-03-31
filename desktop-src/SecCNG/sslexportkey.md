---
description: Retorna protocolo SSL uma chave de sessão de protocolo SSL ou uma chave efêmera pública para um BLOB serializado.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Função SslExportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921409"
---
# <a name="sslexportkey-function"></a>Função SslExportKey

A função **SslExportKey** retorna uma [*chave de sessão*](/windows/desktop/SecGloss/s-gly) de protocolo SSL ou [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) uma chave efêmera pública para um [*blob*](/windows/desktop/SecGloss/b-gly)serializado.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo SSL.

</dd> <dt>

*HKEY* \[ no\]
</dt> <dd>

O identificador da chave a ser exportada.

Quando você não estiver especificando uma chave, defina esse parâmetro como **NULL**.

> [!Note]  
> Um identificador *HKEY* é obtido chamando a função [**SslOpenPrivateKey**](sslopenprivatekey.md) . Não há suporte para identificadores obtidos da função [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .

 

</dd> <dt>

*pszBlobType* \[ no\]
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que contém um identificador que especifica o tipo de BLOB a ser exportado. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ blob público do BCRYPT DH \_**</dt> </dl>    | Exportar uma [*chave pública*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman. O buffer *pbOutput* recebe uma estrutura de [**\_ \_ \_ blob de chave DH BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) imediatamente seguida pelos dados de chave.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BLOB de BCRYPT \_ ECCPUBLIC \_**</dt> </dl>     | Exportar uma chave pública de [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC). O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ ECCKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) imediatamente seguida pelos dados de chave.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_blob de \_ chave \_ opaco de BCRYPT**</dt> </dl> | Exporte uma chave simétrica em um formato específico para um único CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ). BLOBs opacos não são transferível e devem ser importados usando o mesmo CSP ( *provedor de serviços de criptografia* ) que gerou o blob.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BLOB de BCRYPT \_ RSAPUBLIC \_**</dt> </dl>     | Exportar uma chave pública RSA. O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ RSAKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) imediatamente seguida pelos dados de chave.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, opcional\]
</dt> <dd>

O endereço de um buffer que recebe o [*blob de chave*](/windows/desktop/SecGloss/k-gly). O parâmetro *cbOutput* contém o tamanho desse buffer. Se esse parâmetro for **NULL**, essa função coloca o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ fora\]
</dt> <dd>

O endereço de uma variável **DWORD** que recebe o número de bytes copiados para o buffer *pbOutput* . Se o parâmetro *pbOutput* for definido como **NULL** quando a função for chamada, o tamanho necessário para o buffer *pbOutput* , em bytes, será retornado no **DWORD** apontado por esse parâmetro.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

A função **SslExportKey** facilita o transporte de chaves de sessão de um processo para outro, bem como a exportação da parte pública uma chave efêmera.

Ao exportar chaves de sessão, o tipo de BLOB é opaco, o que significa que o formato do BLOB é irrelevante, desde que as funções **SslExportKey** e [**SslImportKey**](sslimportkey.md) possam interpretá-la.

Ao exportar a parte pública de uma chave efêmera, o tipo de BLOB deve ser o tipo apropriado, como **NCrypt do blob público de \_ DH \_ \_** ou do **\_ \_ blob ECCPUBLIC de NCrypt**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

