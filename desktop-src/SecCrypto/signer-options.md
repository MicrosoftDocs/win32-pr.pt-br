---
description: Define ou recupera a opção de certificado do signante.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Propriedade Signer.Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7b4a787524e967b5356ed7fb5531a3ec7d7dbfb99d57fc75217a82f220468db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898832"
---
# <a name="signeroptions-property"></a>Propriedade Signer.Options

\[A **propriedade** Options está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

A **propriedade Options** define ou recupera a opção de certificado do signante.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valor da propriedade

Um valor da [**enumeração CAPICOM \_ CERTIFICATE INCLUDE \_ \_ OPTION**](capicom-certificate-include-option.md) que especifica a opção de certificado do signante. O valor padrão é CAPICOM \_ CERTIFICATE INCLUDE CHAIN EXCEPT \_ \_ \_ \_ ROOT. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CADEIA DE INCLUSÃO DE CERTIFICADO CAPICOM, \_ \_ EXCETO \_ \_ \_ RAIZ**</dt> </dl> | Salva todos os certificados na cadeia com exceção da entidade raiz.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**O CERTIFICADO CAPICOM \_ \_ INCLUI CADEIA \_ \_ INTEIRA**</dt> </dl>                    | Salva a cadeia de certificados completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**O CERTIFICADO CAPICOM \_ \_ INCLUI APENAS ENTIDADE \_ \_ \_ FINAL**</dt> </dl>       | Salva apenas o certificado de entidade final.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Signatário**](signer.md)
</dt> </dl>

 

 
