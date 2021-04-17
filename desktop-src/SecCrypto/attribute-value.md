---
description: Define ou recupera o valor do atributo.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Propriedade Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758282"
---
# <a name="attributevalue-property"></a>Propriedade Attribute. Value

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]

A propriedade **Value** define ou recupera o valor do atributo.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Valor da propriedade

Uma variável **Variant** que contém o valor do atributo. Para atributos de **tempo de \_ \_ \_ assinatura \_ de atributo capicod** , o tipo de dados é **Date**. Para todos os outros atributos, o valor da propriedade é uma cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
