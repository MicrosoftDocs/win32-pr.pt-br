---
description: Representa uma coleção de objetos Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Objeto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61936fff0421c43a07483fb8489cca755154a8cfbdd524da5837b12f90add969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773177"
---
# <a name="attributes-object"></a>Objeto Attributes

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use [**a Classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

O **objeto Attributes** representa uma coleção de objetos [**Attribute.**](attribute.md) Cada [**objeto**](attribute.md) Attribute representa um único atributo de uma mensagem.

## <a name="when-to-use"></a>Quando usar

O **objeto Attributes** é usado para executar as seguintes tarefas:

-   Adicione ou remova um [**objeto Attribute**](attribute.md) específico da coleção.
-   Limpe a coleção.
-   Recupere o número de atributos na coleção.
-   Recupere um [**objeto Attribute**](attribute.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O **objeto Attributes** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto Attributes** tem esses métodos.



| Método                              | Descrição                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Adicionar**](attributes-add.md)       | Adiciona um [**objeto**](attribute.md) Attribute à coleção.<br/>       |
| [**Limpar**](attributes-clear.md)   | Limpa todos os [**objetos Attribute**](attribute.md) da coleção.<br/> |
| [**Remover**](attributes-remove.md) | Remove um [**objeto Attribute**](attribute.md) da coleção.<br/>  |



 

### <a name="properties"></a>Propriedades

O **objeto Attributes** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contagem**](attributes-count.md)<br/>       | Somente leitura<br/> | Recupera o número de [**objetos Attribute**](attribute.md) na coleção.<br/>                                                                                                                                    |
| [**Item**](attributes-item.md)<br/>         | Somente leitura<br/> | Recupera o [**objeto Attribute**](attribute.md) que representa o atributo indexado. Essa é a propriedade padrão.<br/>                                                                                             |



 

## <a name="remarks"></a>Comentários

O **objeto Attributes** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> </dl>

 

 
