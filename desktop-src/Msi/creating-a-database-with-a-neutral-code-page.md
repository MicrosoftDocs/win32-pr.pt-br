---
description: A abordagem recomendada para lidar com páginas de código é criar um banco de dados de base neutro que contenha apenas caracteres que possam ser traduzidos em qualquer página de código.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Criando um banco de dados com uma página de código neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011164"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Criando um banco de dados com uma página de código neutra

A abordagem recomendada para lidar com páginas de código é criar um banco de dados de base neutro que contenha apenas caracteres que possam ser traduzidos em qualquer página de código. O banco de dados pode então ser definido para a página de código da localização e as informações de localização podem ser adicionadas conforme descrito em [localizando um pacote de Windows Installer](localizing-a-windows-installer-package.md).

Para criar um banco de dados neutro, evite caracteres estendidos que não pertençam ao conjunto de caracteres ASCII e, portanto, exijam uma página de código especial. Por exemplo, o sinal de direitos autorais, © e o sinal de marca registrada,, não são caracteres ASCII, e exigem uma página de código ANSI especial para exibição adequada. Em vez disso, use (c) e (r), porque esses caracteres podem ser traduzidos ou transformados para os símbolos para a versão em inglês. Esse banco de dados neutro pode ser localizado definindo sua página de código e adicionando informações de localização por edição de tabela ou Importando arquivos mortos de texto.

 

 



