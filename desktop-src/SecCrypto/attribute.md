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
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811804"
---
# <a name="attribute-object"></a>Objeto Attribute

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]

O objeto de **atributo** representa um único atributo autenticado.

## <a name="when-to-use"></a>Quando usar

O objeto **Attribute** é usado para executar as seguintes tarefas:

-   Defina ou recupere o nome do CAPICOM do atributo.
-   Defina ou recupere o valor do atributo, como a hora de assinatura, o nome do documento assinado ou uma descrição do documento assinado.

## <a name="members"></a>Membros

O objeto de **atributo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **Attribute** tem essas propriedades.



| Propriedade                                    | Tipo de acesso           | Descrição                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Nome**](attribute-name.md)<br/>   | Leitura/gravação<br/> | Define ou recupera o nome do CAPICOM do atributo. Essa é a propriedade padrão.<br/> |
| [**Valor**](attribute-value.md)<br/> | Leitura/gravação<br/> | Define ou recupera o valor do atributo.<br/>                                      |



 

## <a name="remarks"></a>Comentários

O objeto **Attribute** pode ser criado e é seguro para scripts. O ProgID do objeto de **atributo** é CAPICOM. Atributo. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
