---
description: Quando um módulo dá suporte a vários idiomas, você pode mesclá-lo no mesmo banco de dados Windows Instalador várias vezes, mas certifique-se de que cada mesclagem use um idioma diferente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Mesclando um módulo de vários idiomas no mesmo pacote várias vezes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a96f3830b2caa4069eddc69b0b68de1deff35d00c5b4fdb81d4d21d4355bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129256"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Mesclando um módulo de vários idiomas no mesmo pacote várias vezes

Quando um módulo dá suporte a vários idiomas, você pode mesclá-lo no mesmo banco de dados Windows Instalador várias vezes, mas certifique-se de que cada mesclagem use um idioma diferente. Antes de cada mesclagem, solicite um idioma diferente do módulo. O banco .msi banco de dados resultante tem um registro na Tabela [ModuleSignature](modulesignature-table.md) para cada mesclagem do módulo. Componentes compartilhados entre idiomas existem apenas uma vez na Tabela de Componentes [,](component-table.md)mas estão associados a cada idioma na [Tabela ModuleComponents](modulecomponents-table.md).

Ao mesclar vários idiomas de um módulo no mesmo pacote, cada mesclagem deve atender às mesmas restrições em páginas de código que módulos de idioma único. Os módulos não podem conter cadeias de caracteres em páginas de código diferentes.

Ao mesclar um módulo várias vezes em um único arquivo .msi, talvez seja [](file-table.md) necessário modificar a ordem dos arquivos na Tabela de Arquivos para usar o .cab existente do módulo diretamente em sua instalação. A ordem dos arquivos na Tabela de Arquivos deve corresponder à ordem dos arquivos no .cab. Ao mesclar um módulo várias vezes em um banco de dados de instalação, a sequência pode ser modificada, pois os arquivos compartilhados entre os idiomas já podem existir no módulo de uma mesclagem anterior e têm um número de sequência relativo diferente.

 

 



