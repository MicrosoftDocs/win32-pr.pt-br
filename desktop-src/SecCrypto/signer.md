---
description: Estabelece o signatário de um objeto SignedData ou SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objeto de signatário
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758269"
---
# <a name="signer-object"></a>Objeto de signatário

\[O objeto de **signatário** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto de **signatário** estabelece o signatário de um objeto [**SignedData**](signeddata.md) ou [**SignedCode**](signedcode.md) . O [**certificado**](certificate.md) do objeto de **signatário** deve ter uma chave privada disponível que pode ser usada para assinar dados.

## <a name="members"></a>Membros

O objeto de **signatário** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto de **signatário** tem esses métodos.



| Método                      | Descrição                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Carregar**](signer-load.md) | Carrega um certificado de autenticação de um arquivo PFX especificado.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto de **signatário** tem essas propriedades.



| Propriedade                                                                     | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Somente leitura<br/>  | A coleção de atributos autenticados.<br/>                                                                                                                                                                                                                                                                                      |
| [**Certificado**](signer-certificate.md)<br/>                         | Leitura/gravação<br/> | O objeto de [**certificado**](certificate.md) que representa o certificado de um signatário dos dados.<br/> Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido.<br/> Essa é a propriedade padrão.<br/> |
| [**Cadeia**](signer-chain.md)<br/>                                     | Somente leitura<br/>  | A cadeia do signatário.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Opções**](signer-options.md)<br/>                                 | Leitura/gravação<br/> | Define ou recupera a opção de certificado do signatário.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

O objeto de **signatário** pode ser criado e é seguro para scripts. O ProgID do objeto de **signatário** é CAPICOM. Signatário. 2.

**CAPICOM 1. *x*:** o ProgID do objeto de **signatário** é CAPICOM. Signatário. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
