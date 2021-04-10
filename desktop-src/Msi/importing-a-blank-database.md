---
description: Para reproduzir o exemplo, você precisa copiar ou criar com uma ferramenta de software, um arquivo de banco de dados Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importando um banco de dados em branco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170426"
---
# <a name="importing-a-blank-database"></a>Importando um banco de dados em branco

Para reproduzir o exemplo, você precisa copiar ou criar com uma ferramenta de software, um arquivo de banco de dados Windows Installer. Um banco de dados de instalação totalmente em branco, Schema.msi, é fornecido com os [componentes de SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). O SDK também fornece um banco de dados parcialmente em branco, uisample.msi, que contém as tabelas de sequência sugeridas e os requisitos necessários para uma interface de usuário simples. Faça uma cópia do uisample.msi e mova-o para o mesmo diretório que contém a pasta do bloco de notas que você criou no [planejamento da instalação](planning-the-installation.md). Renomeie o arquivo MNP2000.msi. O arquivo de banco de dados de instalação e os arquivos de origem devem estar localizados na raiz do mesmo diretório. Por exemplo:

C: \\MNP2000.msi de exemplo \\

C: \\ bloco de notas de exemplo \\\\

Se você não usar Uisample.msi, deverá obter um banco de dados em branco, como Schema.msi e inserir informações para a instalação usando uma ferramenta de edição de banco de dados, como o orca, que é fornecido com o SDK ou outro editor de banco de dados.

[Continuar](specifying-directory-structure.md)

 

 



