---
description: Durante uma Windows do instalador, o instalador pode pesquisar um arquivo em um local específico no sistema do usuário.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Procurando um arquivo em um local específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b131708e5f9ff37474864aa5d6ef13abcab8f0d162563ca810c7e31fe2c41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041146"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Procurando um arquivo em um local específico

**Para pesquisar um arquivo em um local específico em um sistema de usuário**

1.  Liste a assinatura de arquivo e o nome na [Tabela de Assinatura](signature-table.md). Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.

    [Tabela de assinatura](signature-table.md)

    

    | Assinatura          | Nome do arquivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Insira a propriedade que o Instalador deve definir se MyApp.exe estiver instalado.

    [Tabela AppSearch](appsearch-table.md) (parcial)

    

    | Propriedade         | Assinatura          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Use a [tabela DrLocator](drlocator-table.md). Insira o caminho completo para o arquivo no sistema de usuário no campo Caminho. Insira um valor de 0 na coluna Profundidade para pesquisar a pasta bin.

    [Tabela DrLocator](drlocator-table.md)

    

    | Assinatura          | Pai | Caminho                                                    | Profundidade        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ Compartimento de projetos \\ MyProducts de Arquivos \\ de \\ Programas<br/> | 0<br/> |

    

     

4.  Inclua a ação AppSearch na sequência de ação. Se MyApp.exe estiver instalado no compartimento C: Arquivos de Programas \\ \\ MyProducts Projects, o Instalador define a propriedade MYAPP como \\ o local do \\ arquivo.

 

 




