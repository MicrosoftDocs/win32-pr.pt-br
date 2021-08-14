---
title: Sobre informações de versão
description: Este tópico discute as funções de informações de versão.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- recursos, informações de versão
- informações de versão
- adicionando informações de versão
- conflitos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7b7916e77d29fa21aa6eb68e223d43a1415c36058fbe00e2d3abb9c4cae979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870712"
---
# <a name="about-version-information"></a>Sobre informações de versão

Você pode usar as funções de informações de versão para determinar onde um arquivo deve ser instalado e identificar conflitos com os arquivos atualmente instalados. Essas funções permitem evitar os seguintes problemas:

-   Instalando versões mais antigas de componentes em versões mais recentes
-   alterando o idioma em um sistema de idioma misto sem notificação
-   Instalando várias cópias de uma biblioteca em diretórios diferentes
-   copiando arquivos para diretórios de rede compartilhados por vários usuários

As funções de informações de versão permitem que os aplicativos consultem um recurso de versão para informações de arquivo e apresentem as informações em um formato não criptografado. Essas informações incluem a finalidade do arquivo, o autor, o número de versão e assim por diante.

você pode adicionar informações de versão a todos os arquivos que podem ter Windows recursos, como DLLs, arquivos executáveis ou arquivos de fonte. fon. Para adicionar as informações, crie um [recurso VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) e use o compilador de recurso para compilar o recurso.

 

 