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
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365909"
---
# <a name="about-version-information"></a>Sobre informações de versão

Você pode usar as funções de informações de versão para determinar onde um arquivo deve ser instalado e identificar conflitos com os arquivos atualmente instalados. Essas funções permitem evitar os seguintes problemas:

-   Instalando versões mais antigas de componentes em versões mais recentes
-   alterando o idioma em um sistema de idioma misto sem notificação
-   Instalando várias cópias de uma biblioteca em diretórios diferentes
-   copiando arquivos para diretórios de rede compartilhados por vários usuários

As funções de informações de versão permitem que os aplicativos consultem um recurso de versão para informações de arquivo e apresentem as informações em um formato não criptografado. Essas informações incluem a finalidade do arquivo, o autor, o número de versão e assim por diante.

Você pode adicionar informações de versão a todos os arquivos que podem ter recursos do Windows, como DLLs, arquivos executáveis ou arquivos de fonte. Fon. Para adicionar as informações, crie um [recurso VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) e use o compilador de recurso para compilar o recurso.

 

 