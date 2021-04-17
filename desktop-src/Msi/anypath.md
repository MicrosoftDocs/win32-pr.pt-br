---
description: O tipo de dados AnyPath é uma cadeia de caracteres de texto que contém um caminho completo ou um caminho relativo.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752664"
---
# <a name="anypath"></a>AnyPath

O tipo de dados AnyPath é uma cadeia de caracteres de texto que contém um caminho completo ou um caminho relativo. Ao especificar um caminho relativo, você pode incluir um nome de arquivo longo com o nome curto do arquivo separando os nomes curtos e longos com uma barra vertical ( \| ). Observe que você não pode especificar vários níveis de um diretório ou caminhos totalmente qualificados dessa maneira. O caminho pode conter Propriedades delimitadas entre colchetes ( \[ \] ).

Exemplos de dados de AnyPath válidos:

-   \\\\\\Temp do compartilhamento do servidor \\
-   c: \\ Temp
-   \\Temp
-   proje ~ 1 \| status do projeto

Exemplos de dados de AnyPath inválidos:

-   c: \\ temp \\ proje ~ 1 \| c: \\ Temp um \\ status do projeto
-   \\temp \\ proje ~ 1 \| \\ Temp um \\ status do projeto

 

 



