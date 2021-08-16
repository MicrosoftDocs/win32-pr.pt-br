---
description: O Windows instalador pode executar uma instalação administrativa de um aplicativo ou produto em uma rede para uso por um grupo de trabalho.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Instalação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26968b6b81c1c2aafedfd74151b139f61062baa29c44b04977a119b14ab1a8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381846"
---
# <a name="administrative-installation"></a>Instalação administrativa

O Windows instalador pode executar uma instalação administrativa de um aplicativo ou produto em uma rede para uso por um grupo de trabalho. Uma instalação administrativa instala uma imagem de origem do aplicativo na rede semelhante a uma imagem de origem em um CD-ROM. Os usuários em um grupo de trabalho que têm acesso a essa imagem administrativa podem instalar o produto dessa fonte. Um usuário deve primeiro instalar o produto da rede para executar o aplicativo. O usuário pode optar por executar de origem ao instalar e o instalador usa a maior parte do arquivo do produto diretamente da rede.

Os administradores podem executar uma instalação administrativa na linha de comando usando a opção de linha [de comando](command-line-options.md)/a .

A [ação ADMIN](admin-action.md) é a ação de nível superior usada para iniciar uma instalação administrativa. Quando essa ação é executada, o instalador chama as ações nas tabelas [AdminExecuteSequence](adminexecutesequence-table.md) e [AdminUISequence](adminuisequence-table.md) para executar a instalação administrativa.

A [**propriedade AdminProperties**](adminproperties.md) é uma lista delimitada por ponto e vírgula das propriedades definidas no momento de uma instalação de administração. O instalador usa essas propriedades durante uma instalação pós-administração do aplicativo da imagem administrativa.

Os usuários que não têm acesso contínuo à rede podem instalar um aplicativo de uma imagem administrativa e, às vezes, têm que depender de mídia, como discos CD-ROM, como sua origem de backup. Nesses casos, o comprimento dos nomes de arquivo na imagem administrativa e na mídia deve corresponder. Ambos devem usar nomes de arquivo longos ou ambos devem usar nomes de arquivo curtos. Por exemplo, um CD-ROM que dá suporte apenas a nomes de arquivo curtos pode fornecer a mídia original para instalar a imagem administrativa e uma fonte de backup.

Se a [**propriedade SHORTFILENAMES**](shortfilenames.md) for definida durante uma instalação administrativa, essa propriedade poderá precisar ser definida novamente por um usuário aplicando subsequentemente um patch à imagem administrativa. Ao usar Windows instalador para aplicar o patch, o instalador define automaticamente a propriedade **SHORTFILENAMES** se a imagem administrativa usa nomes de arquivo curtos.

Se um administrador usar um pacote com uma propriedade Resumo de Contagem de [**Palavras**](word-count-summary.md) de 2 ou 3 para executar uma instalação administrativa, os usuários da imagem administrativa não poderão reinstalar automaticamente da fonte de mídia original. Se a imagem administrativa ficar indisponível, os usuários que instalaram a partir da imagem administrativa serão impedidos de reverter para a mídia original.

A aplicação [*de transformaçãos*](t-gly.md) durante a criação de uma imagem administrativa não tem nenhum efeito válido. Para disponibilizar uma versão personalizada de um produto para um grupo de trabalho, aplique a transformação durante a instalação do produto da imagem administrativa.

Durante uma instalação administrativa, o instalador cria uma imagem de origem para todos os recursos do produto, exceto os recursos com 0 na coluna Nível da [tabela Recurso](feature-table.md).

 

 



