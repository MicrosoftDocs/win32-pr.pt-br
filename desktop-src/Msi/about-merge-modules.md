---
description: Os módulos de mesclagem são essencialmente arquivos .msi, que é a extensão de nome de arquivo para um pacote Windows instalação do instalador. Um módulo de mesclagem padrão tem uma extensão de nome de arquivo .msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Sobre módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3e6c0ec1d4d7073d85984539ce54b47de92885a64570bc1de709be64748b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640158"
---
# <a name="about-merge-modules"></a>Sobre módulos de mesclagem

Os módulos de mesclagem são essencialmente arquivos .msi, que é a extensão de nome de arquivo para um pacote Windows instalação do instalador. Um módulo de mesclagem padrão tem uma extensão de nome de arquivo .msm.

Um módulo de mesclagem não pode ser instalado sozinho porque não tem algumas tabelas de banco de dados vitais presentes em um banco de dados de instalação. Os módulos de mesclagem também contêm tabelas adicionais exclusivas para si mesmos. Para instalar as informações entregues por um módulo de mesclagem com um aplicativo, o módulo deve primeiro ser mesclado no arquivo de .msi aplicativo.

Um módulo de mesclagem consiste nas seguintes partes:

-   Um [Banco de Dados de Módulo de](merge-module-database.md) Mesclagem que contém as propriedades de instalação e a lógica de instalação que está sendo entregue pelo módulo de mesclagem.
-   Uma [Referência de Fluxo de Informações de Resumo do Módulo de Mesclagem](merge-module-summary-information-stream-reference.md) que descreve o módulo.
-   Um [MergeModule.CABarquivo de gabinete inet](mergemodule-cabinet.md) armazenado como um fluxo dentro do módulo de mesclagem. Esse gabinete contém todos os arquivos exigidos pelos componentes entregues pelo módulo de mesclagem.

[Vários módulos de mesclagem de idioma](multiple-language-merge-modules.md) podem fornecer componentes para um pacote de instalação em vários idiomas. Em um módulo de mesclagem de vários idiomas, o banco de dados contém as propriedades de instalação e a lógica para mais de um idioma e o gabinete MergeModule.CABinet inclui todos os arquivos necessários para instalar componentes com todos os idiomas com suporte pelo módulo.

 

 



