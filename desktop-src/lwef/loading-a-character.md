---
title: Carregando um caractere
description: Carregando um caractere
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635861"
---
# <a name="loading-a-character"></a>Carregando um caractere

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para animar um caractere, você deve primeiro carregar o caractere. Use o método [**Load**](load-method.md) para carregar os dados do caractere. O Microsoft Agent dá suporte a dois formatos de dados de caractere e animação: um único arquivo estruturado e arquivos separados. Normalmente, você usa o formato de arquivo único (. ACS) quando os dados são armazenados localmente. O formato de vários arquivos (. ACF,. ACA) funciona melhor quando você deseja baixar animações individualmente, como ao acessar animações de um servidor HTTP.

Um aplicativo cliente pode carregar apenas uma única instância do mesmo caractere. Qualquer tentativa de carregar o mesmo caractere mais de uma vez falhará. No entanto, um aplicativo pode ter várias instâncias do mesmo caractere carregado fornecendo conexões separadas ao Microsoft Agent. Por exemplo, um aplicativo pode carregar o mesmo caractere de duas cópias do controle do Microsoft Agent.

Você também pode definir seus próprios caracteres para uso com o Microsoft Agent. Você pode usar qualquer ferramenta de renderização que preferir para criar as imagens, desde que você acabe com arquivos de formato de bitmap do Windows. Para montar e compilar as imagens de um caractere em animações para uso com o Microsoft Agent, use o editor de caracteres do Microsoft Agent. Essa ferramenta permite que você defina as propriedades padrão de um caractere, bem como definir animações para o caractere. O editor de caracteres do Microsoft Agent também permite que você selecione o formato de arquivo apropriado ao criar um caractere.

 

 




