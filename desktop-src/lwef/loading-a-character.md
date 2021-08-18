---
title: Carregando um caractere
description: Carregando um caractere
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78d796df5c1699b405e8cae1dbae0e7d7d8d37932aa50534fa7331a458dc54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748399"
---
# <a name="loading-a-character"></a>Carregando um caractere

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para animar um caractere, você deve primeiro carregar o caractere. Use o método [**Load**](load-method.md) para carregar os dados do caractere. O Microsoft Agent dá suporte a dois formatos de dados de caractere e animação: um único arquivo estruturado e arquivos separados. Normalmente, você usa o formato de arquivo único (. ACS) quando os dados são armazenados localmente. O formato de vários arquivos (. ACF,. ACA) funciona melhor quando você deseja baixar animações individualmente, como ao acessar animações de um servidor HTTP.

Um aplicativo cliente pode carregar apenas uma única instância do mesmo caractere. Qualquer tentativa de carregar o mesmo caractere mais de uma vez falhará. No entanto, um aplicativo pode ter várias instâncias do mesmo caractere carregado fornecendo conexões separadas ao Microsoft Agent. Por exemplo, um aplicativo pode carregar o mesmo caractere de duas cópias do controle do Microsoft Agent.

Você também pode definir seus próprios caracteres para uso com o Microsoft Agent. você pode usar qualquer ferramenta de renderização que preferir para criar as imagens, desde que você acabe com Windows arquivos de formato de bitmap. Para montar e compilar as imagens de um caractere em animações para uso com o Microsoft Agent, use o editor de caracteres do Microsoft Agent. Essa ferramenta permite que você defina as propriedades padrão de um caractere, bem como definir animações para o caractere. O editor de caracteres do Microsoft Agent também permite que você selecione o formato de arquivo apropriado ao criar um caractere.

 

 




