---
description: Como a atualização atualiza os arquivos usados pelo aplicativo, você deve modificar a tabela de arquivos do banco de dados.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Atualizando arquivos e atributos de arquivo para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c1d749a61376d38e8c7793ba5766dd63133bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750211"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Atualizando arquivos e atributos de arquivo para uma atualização

Como a atualização atualiza os arquivos usados pelo aplicativo, você deve modificar a [tabela de arquivos](file-table.md) do banco de dados. Use o Orca Editor de banco de dados que é fornecido com o SDK ou outro editor para abrir MNP2001.msi e insira os dados a seguir na [tabela de arquivos](file-table.md).

[File Table](file-table.md)



| Arquivo         | Componente\_ | FileName     | FileSize | Versão | Idioma | Atributos | Sequência |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Beisebol    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | Concerto     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | Dance       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | Comemorar    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | Quadra  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ajuda        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | Janeiro     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | NewYears    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | Memorial    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloco de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloco de notas     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continuar](updating-components-for-an-upgrade.md)

 

 



