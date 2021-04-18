---
description: Salva o certificado em um arquivo.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'Método ICertificate2:: Save'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796380"
---
# <a name="icertificate2save-method"></a>Método ICertificate2:: Save

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Save** salva o certificado em um arquivo. Esse método foi introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do arquivo de saída no qual o certificado será salvo.

</dd> <dt>

*Senha* \[ do em, opcional\]
</dt> <dd>

Uma cadeia de caracteres que contém a senha de [*texto não criptografado*](../secgloss/p-gly.md) para um arquivo de [*chave privada*](../secgloss/p-gly.md) . A senha pode conter até 32 caracteres Unicode, incluindo um caractere nulo de terminação. Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> <dt>

*Salvar como* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração do [**certificado CAPICOM \_ \_ Salvar \_ como \_ tipo**](capicom-certificate-save-as-type.md) que especifica o formato do arquivo de saída. O padrão é o **CAPICOM de \_ \_ salvar certificado \_ como \_ cer**. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                  | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**\_salvar certificado de CApicom \_ \_ como \_ cer**</dt> </dl> | O arquivo de saída será formatado como um arquivo. cer sem chaves privadas salvas.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**\_salvar certificado de CApicom \_ \_ como \_ pfx**</dt> </dl> | O arquivo de saída será formatado como um arquivo. pfx (PKCS \# 12) e quaisquer chaves privadas associadas que sejam exportáveis também serão salvas.<br/> |



 

</dd> <dt>

*IncludeOption* \[ em, opcional\]
</dt> <dd>

Um valor do [**certificado CAPICOM \_ \_ inclui \_**](capicom-certificate-include-option.md) a enumeração de opção que especifica quantos certificados na cadeia são salvos no arquivo de saída. O padrão é capicor \_ certificado \_ somente inclusão de \_ \_ entidade final \_ . A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM de certificado de caissor \_ \_ \_ \_ , exceto \_ raiz**</dt> </dl> | Salva todos os certificados na cadeia com a exceção da entidade raiz<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**certificado CAPICOM \_ \_ incluir \_ \_ cadeia inteira**</dt> </dl>                    | Salva a cadeia de certificados completa<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**o certificado CAPICOM \_ \_ inclui \_ \_ somente entidade final \_**</dt> </dl>       | Salva apenas o certificado de entidade final<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
