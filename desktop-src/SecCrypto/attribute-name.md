---
description: Define ou recupera o nome do CAPICOM do atributo. Essa é a propriedade padrão.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Propriedade Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3234d02e5e0f68817896f2d0c9d05be25b55bbe97f49fea4d34bafbab627b2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773650"
---
# <a name="attributename-property"></a>Propriedade Attribute.Name

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]

A propriedade **Name** define ou recupera o nome do CAPICOM do atributo. Essa é a propriedade padrão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**do \_ atributo capicor**](capicom-attribute.md) que especifica o nome do CAPICOM do atributo. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                                                 | Significado                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**tempo de assinatura do atributo capicod \_ autenticado \_ \_ \_**</dt> </dl>                         | O atributo contém a hora em que a assinatura foi criada.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**\_nome do documento de atributos autenticados do CApicom \_ \_ \_**</dt> </dl>                      | O atributo contém o nome do documento assinado.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**\_Descrição do documento de atributos autenticados CApicom \_ \_ \_**</dt> </dl> | O atributo contém uma descrição do documento assinado.<br/>    |



 

## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o estado inteiro do objeto é redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributo**](attribute.md)
</dt> </dl>

 

 
