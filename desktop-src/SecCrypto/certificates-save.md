---
description: Salva os objetos de certificado na coleção.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Método Certificates. Save
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3d724a6859a1fbc7765822227290facfb2c2f021fce2f5815f32c5e91fe6453
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126756"
---
# <a name="certificatessave-method"></a>Método Certificates. Save

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Save** salva os objetos de [**certificado**](certificate.md) na coleção.

## <a name="syntax"></a>Sintaxe


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do arquivo de saída onde os certificados serão salvos.

</dd> <dt>

*Senha* \[ do em, opcional\]
</dt> <dd>

Uma cadeia de caracteres que contém a senha de [*texto não criptografado*](../secgloss/p-gly.md) para um arquivo de [*chave privada*](../secgloss/p-gly.md) . O valor padrão é a cadeia de caracteres vazia (""). Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha. Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> <dt>

*Salvar como* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração de [**certificados CAPICOM \_ \_ Salvar \_ como \_ tipo**](capicom-certificates-save-as-type.md) que especifica o formato do arquivo de saída. O padrão é capicor \_ certificados \_ Save \_ as \_ PFX. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                          | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**os certificados CAPICOM \_ \_ Salvar \_ como \_ pfx**</dt> </dl>                      | Os certificados são salvos como um PFX.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**Os certificados CAPICOM \_ \_ Save \_ as \_ PKCS7**</dt> </dl>                | Os certificados são salvos como um PKCS \# 7.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**os certificados CAPICOM \_ \_ Salvar \_ como \_ serializado**</dt> </dl> | Os certificados são salvos como serializados.<br/> |



 

</dd> <dt>

*ExportFlag* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ sinalizador de exportação de CAPICOM**](capicom-export-flag.md) que especifica se os erros de exportação de chave privada são ignorados. O padrão é o CAPICOM de \_ exportação \_ padrão. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                                                          | Significado                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**\_padrão de exportação de CApicom \_**</dt> </dl>                                                                                                      | Os erros de exportação de chave privada não são ignorados.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**\_erro de exportação para \_ ignorar \_ \_ chave privada \_ não \_ exportável \_ do CAPICOM**</dt> </dl> | Erros de exportação de chave privada são ignorados.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

Os objetos de [**certificado**](certificate.md) podem ser recuperados usando o método [**Store. Load**](store-load.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
