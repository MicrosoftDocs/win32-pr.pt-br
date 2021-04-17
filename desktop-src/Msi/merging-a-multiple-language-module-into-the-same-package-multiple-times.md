---
description: Quando um módulo dá suporte a vários idiomas, você pode mesclá-lo no mesmo Windows Installer banco de dados várias vezes, mas certifique-se de que cada mesclagem usa um idioma diferente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Mesclar um módulo de vários idiomas no mesmo pacote várias vezes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792496"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Mesclar um módulo de vários idiomas no mesmo pacote várias vezes

Quando um módulo dá suporte a vários idiomas, você pode mesclá-lo no mesmo Windows Installer banco de dados várias vezes, mas certifique-se de que cada mesclagem usa um idioma diferente. Antes de cada mesclagem, solicite um idioma diferente do módulo. O banco de dados. msi resultante tem um registro na [tabela ModuleSignature](modulesignature-table.md) para cada mesclagem do módulo. Os componentes compartilhados entre os idiomas existem apenas uma vez na [tabela de componentes](component-table.md), mas são associados a cada idioma na [tabela ModuleComponents](modulecomponents-table.md).

Ao mesclar vários idiomas de um módulo no mesmo pacote, cada mesclagem deve satisfazer as mesmas restrições em páginas de código como módulos de linguagem única. Os módulos não podem conter cadeias de caracteres em páginas de código diferentes.

Ao mesclar um módulo várias vezes em um único arquivo. msi, talvez seja necessário modificar a ordem dos arquivos na tabela de [arquivos](file-table.md) para usar o. cab existente do módulo diretamente em sua instalação. A ordem dos arquivos na tabela de arquivos deve corresponder à ordem dos arquivos no. cab. Ao mesclar um módulo várias vezes em um banco de dados de instalação, a sequência pode ser modificada, pois os arquivos compartilhados entre os idiomas podem já existir no módulo de uma mesclagem anterior e têm um número de sequência relativo diferente.

 

 



