---
description: A abordagem recomendada para lidar com páginas de código é a de um banco de dados base neutro que contenha apenas caracteres que podem ser convertidos em qualquer página de código.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Criando um banco de dados com uma página de código neutro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e9283378d003adf3069e2feb505fab36c9a379de4deb2a767d10559d547e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379411"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Criando um banco de dados com uma página de código neutro

A abordagem recomendada para lidar com páginas de código é a de um banco de dados base neutro que contenha apenas caracteres que podem ser convertidos em qualquer página de código. Em seguida, o banco de dados pode ser definido como a página de código da localização e as informações de localização podem ser adicionadas, conforme descrito em Localizando um pacote [Windows instalador.](localizing-a-windows-installer-package.md)

Para criar um banco de dados neutro, evite caracteres estendidos que não pertencem ao conjunto de caracteres ASCII e, portanto, exigem uma página de código especial. Por exemplo, o sinal de direitos autorais, © e o sinal de marca registrada, , não são caracteres ASCII e exigem uma página de código ANSI especial para exibição adequada. Em vez disso, use (c) e (r), porque esses caracteres podem ser convertidos ou transformados nos símbolos da versão do idioma inglês. Esse banco de dados neutro pode ser localizado definindo sua página de código e adicionando informações de localização por edição de tabela ou importando arquivos de arquivo de texto.

 

 



