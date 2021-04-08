---
description: O Windows Installer pode executar uma instalação administrativa de um aplicativo ou produto em uma rede para uso por um grupo de trabalho.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Instalação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3958bdc81ee43cd1a36e0d464f3e77032b4c2d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010918"
---
# <a name="administrative-installation"></a>Instalação administrativa

O Windows Installer pode executar uma instalação administrativa de um aplicativo ou produto em uma rede para uso por um grupo de trabalho. Uma instalação administrativa instala uma imagem de origem do aplicativo na rede que é semelhante a uma imagem de origem em um CD-ROM. Os usuários em um grupo de trabalho que têm acesso a essa imagem administrativa podem instalar o produto dessa fonte. Um usuário deve primeiro instalar o produto da rede para executar o aplicativo. O usuário pode optar por executar a origem quando ele instala o e o instalador usa a maior parte do arquivo do produto diretamente da rede.

Os administradores podem executar uma instalação administrativa na linha de comando usando a [opção de linha de comando](command-line-options.md)/a.

A [ação de administrador](admin-action.md) é a ação de nível superior usada para iniciar uma instalação administrativa. Quando essa ação é executada, o instalador chama as ações nas tabelas [AdminExecuteSequence](adminexecutesequence-table.md) e [AdminUISequence](adminuisequence-table.md) para executar a instalação administrativa.

A propriedade [**adminproperties**](adminproperties.md) é uma lista delimitada por ponto e vírgula de propriedades que são definidas no momento de uma instalação de administração. O instalador usa essas propriedades durante uma instalação de administração posterior do aplicativo da imagem administrativa.

Os usuários que não têm acesso contínuo à rede podem instalar um aplicativo de uma imagem administrativa e, em seguida, às vezes precisam contar com mídia, como discos de CD-ROM, como sua fonte de backup. Nesses casos, o comprimento dos nomes de arquivo na imagem administrativa e na mídia deve corresponder. Ambos devem usar nomes de arquivo longos ou ambos devem usar nomes de arquivo curtos. Por exemplo, um CD-ROM que dá suporte apenas a nomes de arquivo curtos pode fornecer a mídia original para instalar a imagem administrativa e uma fonte de backup.

Se a propriedade [**SHORTFILENAMES**](shortfilenames.md) for definida durante uma instalação administrativa, essa propriedade poderá precisar ser definida novamente por um usuário, subseqüentemente aplicando um patch à imagem administrativa. Ao usar Windows Installer para aplicar o patch, o instalador definirá automaticamente a propriedade **SHORTFILENAMES** se a imagem administrativa usar nomes de arquivo curtos.

Se um administrador usar um pacote com uma propriedade de [**Resumo de contagem de palavras**](word-count-summary.md) 2 ou 3 para executar uma instalação administrativa, os usuários da imagem administrativa não poderão reinstalar automaticamente a partir da fonte de mídia original. Se a imagem administrativa ficar indisponível, os usuários que tiverem instalado a partir da imagem administrativa serão impedidos de reverter para a mídia original.

A aplicação de [*transformações*](t-gly.md) durante a criação de uma imagem administrativa não tem nenhum efeito válido. Para tornar uma versão personalizada de um produto disponível para um grupo de trabalho, aplique a transformação durante a instalação do produto da imagem administrativa.

Durante uma instalação administrativa, o instalador cria uma imagem de origem para todos os recursos no produto, exceto o recurso com 0 na coluna nível da [tabela de recursos](feature-table.md).

 

 



