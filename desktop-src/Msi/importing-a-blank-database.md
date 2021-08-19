---
description: Para reproduzir o exemplo que você precisa copiar ou criar com uma ferramenta de software, um arquivo Windows banco de dados do Instalador.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importando um banco de dados em branco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3d2c0a7b0fa8d6364a9eef66b830f94e3523c2dfece9c6e1ec459d146ace11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946593"
---
# <a name="importing-a-blank-database"></a>Importando um banco de dados em branco

Para reproduzir o exemplo que você precisa copiar ou criar com uma ferramenta de software, um arquivo Windows banco de dados do Instalador. Um banco de dados de instalação totalmente em branco, Schema.msi, é fornecido com os componentes do SDK do Windows para desenvolvedores do [Windows Installer.](platform-sdk-components-for-windows-installer-developers.md) O SDK também fornece um banco de dados parcialmente em branco, uisample.msi, que contém as tabelas de sequência sugeridas e os dados necessários para uma interface do usuário simples. Faça uma cópia do uisample.msi e mova-o para o mesmo diretório que contém a pasta Bloco de notas criada em [Planejando a instalação](planning-the-installation.md)do . Renomeie o arquivo MNP2000.msi. O arquivo de banco de dados de instalação e os arquivos de origem devem estar localizados na raiz do mesmo diretório. Por exemplo:

C: \\ Exemplo \\ deMNP2000.msi

C: \\ Exemplo \\ de Bloco de notas\\

Se você não usar o Uisample.msi, deverá obter um banco de dados em branco, como Schema.msi, e inserir informações para a instalação usando uma ferramenta de edição de banco de dados, como Orca, fornecida com o SDK ou outro editor de banco de dados.

[Continuar](specifying-directory-structure.md)

 

 



