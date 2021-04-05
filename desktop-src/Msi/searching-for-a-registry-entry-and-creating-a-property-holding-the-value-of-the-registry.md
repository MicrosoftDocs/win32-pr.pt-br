---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar uma entrada de registro e criar uma propriedade que contém o valor do registro.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Procurando uma entrada de registro e criando uma propriedade que contém o valor do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826849"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>Procurando uma entrada de registro e criando uma propriedade que contém o valor do registro

**Para procurar uma entrada de registro e criar uma propriedade que contém o valor desse arquivo**

1.  Não adicione a assinatura à tabela de [assinatura](signature-table.md) ou à [tabela CompLocator](complocator-table.md). Se uma assinatura de arquivo estiver listada na [tabela AppSearch](appsearch-table.md) e não estiver listada nas tabelas Signature ou CompLocator, o instalador procurará na [tabela RegLocator](reglocator-table.md).

2.  Especifique a entrada do registro a ser pesquisada na [tabela RegLocator](reglocator-table.md). Se a assinatura estiver ausente da [tabela de assinatura](signature-table.md) e o valor da coluna de tipo for **msidbLocatorTypeRawValue**, a pesquisa será considerada para o nome da chave do registro específico apontado pela tabela RegLocator.

    [Tabela RegLocator](reglocator-table.md) (parcial)

    

    | Signature\_         | Root         | Chave                                                           | Nome                  | Tipo                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | AppValue<br/> | 2<br/> | **Software** \\ **Microsoft** \\ **MyApp**<br/> <br/> | **Myname**<br/> | **msidbLocatorTypeRawValue**<br/> |

    

     

3.  Por fim, preencha a [tabela AppSearch](appsearch-table.md) para que a [ação AppSearch](appsearch-action.md) retorne o valor de AppValue. Depois que o instalador executa a ação AppSearch, o valor de MYREGVAL é o valor de AppValue.

    [Tabela AppSearch](appsearch-table.md) (parcial)

    

    | Propriedade            | Assinatura           |
    |---------------------|---------------------|
    | MYREGVAL<br/> | AppValue<br/> |

    

     

 

 




