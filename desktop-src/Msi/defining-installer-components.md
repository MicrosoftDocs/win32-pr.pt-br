---
description: o seguinte descreve como organizar seu aplicativo em Windows Installer componentes.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definindo componentes do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83d5fa02182c40fa209453484db23706db2f261f41324cd4d86894d9e78dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979556"
---
# <a name="defining-installer-components"></a>Definindo componentes do instalador

o seguinte descreve como organizar seu aplicativo em Windows Installer componentes.

**Para organizar um aplicativo em componentes**

1.  Comece obtendo um diretório e uma árvore de arquivos para todos os arquivos e outros recursos usados em seu aplicativo.
2.  Identifique todos os arquivos, chaves do registro, atalhos ou outros recursos que são compartilhados entre aplicativos e que podem ser fornecidos por componentes existentes disponíveis como [módulos de mesclagem](merge-modules.md). Você não deve incluir nenhum desses recursos nos componentes que criar. Em vez disso, obtenha esses componentes mesclando os módulos de mesclagem em seu pacote de instalação. As etapas a seguir descrevem como organizar os recursos restantes do aplicativo em componentes do.
3.  Defina um novo componente para cada .exe, .dll e arquivo. ocx. Designe esses arquivos como os arquivos de caminho de chave de seus componentes. Atribua a cada componente um GUID de código de componente.
4.  Defina um novo componente para cada arquivo de ajuda. hlp ou. chm. Designe esses arquivos como os arquivos de caminho de chave de seus componentes. Adicione os arquivos. CNT ou. Chi aos componentes que contêm seus arquivos. hlp e. chm associados. Atribua a cada componente um GUID de código de componente.
5.  Defina um novo componente para cada arquivo que serve como um destino de um atalho. Designe esses arquivos como os arquivos de caminho de chave de seus componentes. Atribua a cada componente um GUID de código de componente.
6.  Agrupe todos os recursos restantes em pastas. Todos os recursos em cada pasta devem ser enviados juntos. Se houver uma possibilidade de que um par de recursos possa ser entregue separadamente no futuro, coloque-os em pastas separadas. Defina um novo componente para cada pasta. Tente manter o número total de componentes baixo para melhorar o desempenho. Divida o aplicativo em muitos componentes quando for necessário que o instalador Verifique a validade da instalação completamente. Designar qualquer arquivo no componente como o arquivo de caminho de chave. Atribua a cada componente um GUID de código de componente.
7.  Adicione chaves do registro aos componentes. Qualquer chave do registro que aponte para um arquivo deve ser incluída no componente desse arquivo. Outras chaves do registro devem ser logicamente agrupadas com os arquivos que as exigem.

 

 



