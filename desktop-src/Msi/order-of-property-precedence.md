---
description: O instalador define as propriedades usando a ordem de precedência a seguir. Um valor de propriedade nessa lista pode substituir um valor que vem depois dele e ser substituído por um valor que vem antes dele na lista.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Ordem de precedência de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760837"
---
# <a name="order-of-property-precedence"></a>Ordem de precedência de propriedade

O instalador define as propriedades usando a ordem de precedência a seguir. Um valor de propriedade nessa lista pode substituir um valor que vem depois dele e ser substituído por um valor que vem antes dele na lista.

1.  Propriedades especificadas pelo ambiente operacional.
2.  [Propriedades públicas](public-properties.md) definidas na linha de comando.
3.  Propriedades públicas listadas pelo propriedade [**adminproperties**](adminproperties.md) durante uma [instalação administrativa](administrative-installation.md) .
4.  Propriedades públicas ou privadas definidas durante a aplicação de uma [*transformação*](t-gly.md).
5.  Propriedade pública ou privada que é definida pela criação da [tabela de propriedades](property-table.md) do arquivo. msi.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> </dl>

 

 



