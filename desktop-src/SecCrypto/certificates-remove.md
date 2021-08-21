---
description: Remove um único objeto Certificate da coleção.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: Método ICertificates2::Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 72ab0624784078b2c496032639c371280ff0019ac957d3c579e2c3c9080629bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770427"
---
# <a name="icertificates2remove-method"></a>Método ICertificates2::Remove

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método Remove** remove um único objeto [**Certificate**](certificate.md) da coleção. Esse método foi introduzido no CAPICOM 2.0.

## <a name="syntax"></a>Sintaxe


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ Em\]
</dt> <dd>

Valor de índice para [**o objeto Certificate**](certificate.md) a ser removido. Esse parâmetro pode ser um dos seguintes tipos possíveis.



| Type                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <dt>****Long****</dt><dt></dt> </dl>                                                | O [**objeto**](certificate.md) Certificate no índice especificado na coleção é removido.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>****Cadeia de caracteres****</dt><dt></dt> </dl>                                        | O primeiro [**objeto Certificate**](certificate.md) na coleção que corresponde à impressão digital [*SHA-1*](../secgloss/s-gly.md) contida na cadeia de caracteres especificada é removido.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Certificado**](certificate.md)**</dt><dt></dt> </dl> | O primeiro [**objeto Certificate**](certificate.md) na coleção que corresponde ao objeto **Certificate** especificado é removido.<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
