---
description: Representa uma coleção de objetos de atributo.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Objeto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756157"
---
# <a name="attributes-object"></a>Objeto Attributes

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **Attributes** representa uma coleção de objetos [**Attribute**](attribute.md) . Cada objeto de [**atributo**](attribute.md) representa um único atributo de uma mensagem.

## <a name="when-to-use"></a>Quando usar

O objeto **Attributes** é usado para executar as seguintes tarefas:

-   Adicionar ou remover um objeto de [**atributo**](attribute.md) específico da coleção.
-   Limpe a coleção.
-   Recupere o número de atributos na coleção.
-   Recupere um objeto de [**atributo**](attribute.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **Attributes** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Attributes** tem esses métodos.



| Método                              | Descrição                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Agrega**](attributes-add.md)       | Adiciona um objeto de [**atributo**](attribute.md) à coleção.<br/>       |
| [**Formatação**](attributes-clear.md)   | Limpa todos os objetos de [**atributo**](attribute.md) da coleção.<br/> |
| [**Remover**](attributes-remove.md) | Remove um objeto de [**atributo**](attribute.md) da coleção.<br/>  |



 

### <a name="properties"></a>Propriedades

O objeto **Attributes** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](attributes-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos de [**atributo**](attribute.md) na coleção.<br/>                                                                                                                                    |
| [**Item**](attributes-item.md)<br/>         | Somente leitura<br/> | Recupera o objeto de [**atributo**](attribute.md) que representa o atributo indexado. Essa é a propriedade padrão.<br/>                                                                                             |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto **Attributes** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> </dl>

 

 
