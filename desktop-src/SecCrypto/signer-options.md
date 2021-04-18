---
description: Define ou recupera a opção de certificado do signatário.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Propriedade signatário. Options
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
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753392"
---
# <a name="signeroptions-property"></a>Propriedade signatário. Options

\[A propriedade **Options** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **Options** define ou recupera a opção de certificado do signatário.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valor da propriedade

Um valor do [**certificado CAPICOM \_ \_ inclui \_**](capicom-certificate-include-option.md) a enumeração de opção que especifica a opção de certificado do signatário. O valor padrão é capicor certificado de caminhagem \_ \_ \_ \_ , exceto \_ raiz. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM de certificado de caissor \_ \_ \_ \_ , exceto \_ raiz**</dt> </dl> | Salva todos os certificados na cadeia com a exceção da entidade raiz.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**certificado CAPICOM \_ \_ incluir \_ \_ cadeia inteira**</dt> </dl>                    | Salva a cadeia de certificados completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**o certificado CAPICOM \_ \_ inclui \_ \_ somente entidade final \_**</dt> </dl>       | Salva apenas o certificado de entidade final.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Signatário**](signer.md)
</dt> </dl>

 

 
