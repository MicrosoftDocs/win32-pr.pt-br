---
description: Representa um único atributo autenticado.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Objeto Attribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3e07c771a34e89cfbcbba5695450e195ef55482e0a27bee008f3ea8251bf8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879866"
---
# <a name="attribute-object"></a>Objeto Attribute

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use [**a Classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.**](/previous-versions/windows/)\]

O **objeto** Attribute representa um único atributo autenticado.

## <a name="when-to-use"></a>Quando usar

O **objeto** Attribute é usado para executar as seguintes tarefas:

-   Definir ou recuperar o nome CAPICOM do atributo.
-   Definir ou recuperar o valor do atributo, como a hora de assinatura, o nome do documento assinado ou uma descrição do documento assinado.

## <a name="members"></a>Membros

O **objeto** Attribute tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto** Attribute tem essas propriedades.



| Propriedade                                    | Tipo de acesso           | Descrição                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Nome**](attribute-name.md)<br/>   | Leitura/gravação<br/> | Define ou recupera o nome CAPICOM do atributo. Essa é a propriedade padrão.<br/> |
| [**Valor**](attribute-value.md)<br/> | Leitura/gravação<br/> | Define ou recupera o valor do atributo.<br/>                                      |



 

## <a name="remarks"></a>Comentários

O **objeto** Attribute pode ser criado e é seguro para scripts. O ProgID para o **objeto Attribute** é CAPICOM. Attribute.1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
