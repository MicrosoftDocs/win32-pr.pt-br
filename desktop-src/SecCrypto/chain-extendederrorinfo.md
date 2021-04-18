---
description: Retorna uma cadeia de caracteres que contém informações de erro adicionais sobre a entrada indexada.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'Método IChain2:: ExtendedErrorInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800086"
---
# <a name="ichain2extendederrorinfo-method"></a>Método IChain2:: ExtendedErrorInfo

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **ExtendedErrorInfo** retorna uma cadeia de caracteres que contém informações de erro adicionais sobre a entrada indexada.

Esse método é introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do em, opcional\]
</dt> <dd>

Um **longo** que representa o índice da entrada. O valor padrão é 1, que retorna informações de erro para o certificado final na cadeia. **Certificados. Count** retorna informações sobre o certificado raiz da cadeia. 0 retorna informações de erro estendidas para toda a cadeia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma cadeia de caracteres que contém as informações de erro estendidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Cadeia**](chain.md)
</dt> </dl>

 

 
