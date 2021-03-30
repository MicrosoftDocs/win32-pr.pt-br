---
title: Armazenamentos e fluxos
description: Um objeto de armazenamento é análogo a um diretório do sistema de arquivos.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635186"
---
# <a name="storages-and-streams"></a>Armazenamentos e fluxos

Um objeto de armazenamento é análogo a um diretório do sistema de arquivos. Assim como um diretório pode conter outros diretórios e arquivos, um objeto de armazenamento pode conter outros objetos de armazenamento e objetos de fluxo. Também como um diretório, um objeto de armazenamento controla os locais e os tamanhos dos objetos de armazenamento e os objetos de fluxo aninhados abaixo dele.

Um objeto de fluxo é análogo à noção tradicional de um arquivo. Como um arquivo, um fluxo contém dados armazenados como uma sequência consecutiva de bytes.

Um arquivo composto COM consiste em um objeto de armazenamento raiz contendo pelo menos um objeto de fluxo representando seus dados nativos junto com um ou mais objetos de armazenamento correspondentes aos seus objetos vinculados e incorporados. O objeto de armazenamento raiz é mapeado para um nome de arquivo em qualquer sistema de arquivos que ele esteja residindo. Cada um dos objetos dentro do documento também é representado por um objeto de armazenamento que contém um ou mais objetos Stream, e talvez também contenha um ou mais objetos de armazenamento. Dessa forma, um documento pode consistir em um número ilimitado de objetos aninhados. Para obter mais informações, consulte [arquivos compostos](compound-files.md).

 

 




