---
title: Objetos e propriedades
description: As características de um objeto no SDO são determinadas pelas propriedades do objeto e os valores associados a essas propriedades.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789627"
---
# <a name="objects-and-properties"></a>Objetos e propriedades

As características de um objeto no SDO são determinadas pelas propriedades do objeto e os valores associados a essas propriedades. Ao contrário de alguns outros modelos de objeto, os objetos SDO em si não têm métodos. No entanto, os objetos SDO expõem interfaces COM que fornecem métodos.

Os objetos em SDO expõem a interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) que fornece métodos para manipular as propriedades de objetos. Para acessar as propriedades do objeto, obtenha uma interface **ISdo** para o objeto e use os métodos de interface [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) e [**putProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) para recuperar e definir valores para as propriedades. O tópico [recuperando um usuário SDO contém um](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) código de exemplo que demonstra a obtenção da interface **ISdo** para um objeto de usuário.

Depois de fazer alterações nas propriedades de um objeto, use o método [**ISdo:: apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) para gravar as alterações no armazenamento persistente do objeto. Você pode cancelar as alterações feitas nas propriedades de um objeto antes de chamar **ISdo:: apply** chamando o método [**ISdo:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) . Esse método restaura os valores das propriedades de um objeto do armazenamento persistente.

A tabela a seguir mostra os tipos de enumeração que enumeram as propriedades de alguns dos objetos em SDO.



| Objeto                                 | Tipo de enumeração                                       |
|----------------------------------------|--------------------------------------------------------|
| Todos os objetos SDO                        | [**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| Objeto de usuário                            | [**USERproperties**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Objeto de serviço (servidor de políticas de rede) | [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Objeto de protocolo RADIUS da Microsoft       | [**RADIUSproperties**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.

 

## <a name="collections"></a>Coleções

Os objetos geralmente são agrupados em coleções. A API de SDO fornece funcionalidade, por meio da interface de [**coleção ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , para enumerar os objetos em uma coleção e para adicionar e excluir objetos de uma coleção.

O acesso a uma coleção é obtido pela recuperação de uma propriedade de coleção no objeto que contém a coleção. Para obter mais informações, consulte a seção [hierarquia de modelo de objeto](/windows/desktop/Nps/sdo-object-model-hierarchy).

O tipo de dados para todas as propriedades que correspondem às coleções é expedição de VT \_ .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hierarquia de modelo de objeto SDO](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Atributos com suporte a SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 