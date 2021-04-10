---
description: Os módulos de mesclagem fornecem um método padrão pelo qual os desenvolvedores fornecem componentes de Windows Installer compartilhados e a lógica de instalação para seus aplicativos.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Mesclar módulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171832"
---
# <a name="merge-modules"></a>Mesclar módulos

Os módulos de mesclagem fornecem um método padrão pelo qual os desenvolvedores fornecem [*componentes*](c-gly.md) de Windows Installer compartilhados e a lógica de instalação para seus aplicativos. Os módulos de mesclagem são usados para fornecer código compartilhado, arquivos, recursos, entradas de registro e lógica de instalação para aplicativos como um único arquivo composto. Os desenvolvedores que criam novos módulos de mesclagem ou usam módulos de mesclagem existentes devem seguir o padrão descrito nesta seção.

Um módulo de mesclagem é semelhante na estrutura a um [*arquivo Windows Installer. msi*](m-gly.md)simplificado. No entanto, um módulo de mesclagem não pode ser instalado sozinho, ele deve ser mesclado em um pacote de instalação usando uma ferramenta de mesclagem. Os desenvolvedores que desejam usar módulos de mesclagem devem obter uma das ferramentas de mesclagem distribuídas livremente, como Mergemod.dll ou comprar uma ferramenta de mesclagem de um fornecedor de software independente. Os desenvolvedores podem criar novos módulos de mesclagem usando muitas das mesmas ferramentas de software usadas para criar um pacote de instalação Windows Installer, como o editor de tabela de banco de dados Orca fornecido com o SDK do Windows Installer.

Quando um módulo de mesclagem é mesclado no arquivo. msi de um aplicativo, todas as informações e os recursos necessários para instalar os componentes entregues pelo módulo de mesclagem são incorporados ao arquivo. msi do aplicativo. O módulo de mesclagem não é mais necessário para instalar esses componentes e o módulo de mesclagem não precisa estar acessível a um usuário. Como todas as informações necessárias para instalar os componentes são entregues como um único arquivo, o uso de módulos de mesclagem pode eliminar muitas instâncias de conflitos de versão, entradas de registro ausentes e arquivos instalados incorretamente.

Para obter mais informações sobre módulos de mesclagem, consulte:

-   [Sobre módulos de mesclagem](about-merge-modules.md)
-   [Usando módulos de mesclagem](using-merge-modules.md)
-   [Referência de módulo de mesclagem](merge-module-reference.md)

 

 



