---
description: Módulos de mesclagem são essencialmente arquivos. msi simplificados, que é a extensão de nome de arquivo para um pacote de instalação Windows Installer. Um módulo de mesclagem padrão tem uma extensão de nome de arquivo. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Sobre módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296683"
---
# <a name="about-merge-modules"></a>Sobre módulos de mesclagem

Módulos de mesclagem são essencialmente arquivos. msi simplificados, que é a extensão de nome de arquivo para um pacote de instalação Windows Installer. Um módulo de mesclagem padrão tem uma extensão de nome de arquivo. msm.

Um módulo de mesclagem não pode ser instalado sozinho porque não tem algumas tabelas de banco de dados vitais que estão presentes em um banco de dados de instalação. Os módulos de mesclagem também contêm tabelas adicionais que são exclusivas a si mesmas. Para instalar as informações entregues por um módulo de mesclagem com um aplicativo, o módulo deve primeiro ser mesclado no arquivo. msi do aplicativo.

Um módulo de mesclagem consiste nas seguintes partes:

-   Um [banco de dados de módulo de mesclagem](merge-module-database.md) que contém as propriedades de instalação e a lógica de instalação sendo fornecida pelo módulo de mesclagem.
-   Uma [referência de fluxo de informações resumidas do módulo de mesclagem](merge-module-summary-information-stream-reference.md) que descreve o módulo.
-   Um arquivo de gabinete [MergeModule.CABinet](mergemodule-cabinet.md) armazenado como um fluxo dentro do módulo de mesclagem. Esse gabinete contém todos os arquivos exigidos pelos componentes fornecidos pelo módulo de mesclagem.

[Vários módulos de mesclagem de idiomas](multiple-language-merge-modules.md) podem fornecer componentes para um pacote de instalação em vários idiomas. Em um módulo de mesclagem de vários idiomas, o banco de dados contém as propriedades de instalação e a lógica para mais de um idioma e o MergeModule.CABgabinete inet inclui todos os arquivos necessários para instalar os componentes com todos os idiomas com suporte no módulo.

 

 



