---
title: Controle de acesso e operações de gravação
description: As modificações de propriedade falharão se o chamador não tiver direitos suficientes.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Controle de acesso e operações de gravador AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823623"
---
# <a name="access-control-and-write-operations"></a>Controle de acesso e operações de gravação

As modificações de propriedade falharão se o chamador não tiver direitos suficientes. Para operações de gravação que modificam o lote para várias propriedades, toda a operação falhará se o chamador não tiver os direitos necessários para uma única das propriedades modificadas. Por exemplo, você pode fazer várias chamadas [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para definir várias propriedades em um objeto. No entanto, quando você chamar [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para gravar os novos dados do cache local no diretório, o **setinfo** falhará se o chamador não tiver acesso de gravação a todas as propriedades modificadas. Da mesma forma, o método [**IDirectoryObject:: Setobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) falha ao definir qualquer propriedade se o chamador não tiver acesso a todas as propriedades que estão sendo definidas. Portanto, você deve enviar várias operações de modificação em lote apenas se souber que todas as modificações terão sucesso. Para determinar os atributos de um objeto de diretório que o chamador tem a capacidade de modificar, leia o atributo **allowedAttributesEffective** do objeto.

Se o chamador não tiver direitos suficientes para modificar uma propriedade, os códigos de retorno a seguir poderão ser retornados:

Propriedade \_ de \_ ADS \_ não \_ definida e \_ \_ Propriedade ADS \_ não \_ modificada

 

 