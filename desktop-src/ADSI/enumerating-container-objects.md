---
title: Enumerando objetos de contêiner
description: Por convenção, todos os itens em uma enumeração em ADSI devem ser do mesmo tipo de dados de automação. Por exemplo, uma enumeração não deve retornar alguns itens como uma variante do tipo VT \_ i4 e outros como uma variante do tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff6bb6d05a34ce6434531338a877d2dd4aaee2cd4df0b38c81b50b7f56db4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428555"
---
# <a name="enumerating-container-objects"></a>Enumerando objetos de contêiner

Por convenção, todos os itens em uma enumeração em ADSI devem ser do mesmo tipo de dados de automação. Por exemplo, uma enumeração não deve retornar alguns itens como uma **variante** do tipo **VT \_ i4** e outros como uma **variante** do tipo **VT \_ BSTR**.

Para enumerar uma lista de itens que um objeto mantém, um cliente solicita a criação de um objeto de enumeração para o tipo específico de informações que estão sendo listadas. No ADSI, o cliente pode listar os objetos em objetos de namespace, objetos de contêiner genéricos, objetos de coleção, objetos de membro ou objetos de esquema. A ADSI fornece um filtro que pode ser definido e modificado para limitar as correspondências em qualquer enumeração, por meio da propriedade [**IADsContainer. Filter**](iadscontainer-property-methods.md) . Exemplos de implementações de objetos enumeradores podem ser encontrados no código do componente do provedor de exemplo para os seguintes objetos de contêiner do ADs.



| Tipo de objeto         | code         |
|---------------------|--------------|
| Contêiner genérico   | cenumobj. cpp |
| Contêiner de namespace | cenumns. cpp  |
| Contêiner de esquema    | cenumsch. cpp |



 

Para obter informações do lado do cliente, consulte [coleções e grupos](collections-and-groups.md).

 

 




