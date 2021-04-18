---
description: Remove um único objeto de certificado da coleção.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'Método ICertificates2:: Remove'
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
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758017"
---
# <a name="icertificates2remove-method"></a>Método ICertificates2:: Remove

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Remove** remove um único objeto de [**certificado**](certificate.md) da coleção. Esse método foi introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Valor de índice do objeto de [**certificado**](certificate.md) a ser removido. Esse parâmetro pode ser um dos seguintes tipos possíveis.



| Type                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <dt>* * * * Long * * * *</dt><dt></dt> </dl>                                                | O objeto de [**certificado**](certificate.md) no índice especificado na coleção é removido.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> * * * * <dt>Cadeia de caracteres *</dt> * * *<dt></dt> </dl>                                        | O primeiro objeto de [**certificado**](certificate.md) na coleção que corresponde à impressão digital [*SHA-1*](../secgloss/s-gly.md) contido na cadeia de caracteres especificada é removido.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Certificado**](certificate.md)**</dt> do <dt></dt> </dl> | O primeiro objeto de [**certificado**](certificate.md) na coleção que corresponde ao objeto de **certificado** especificado é removido.<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
