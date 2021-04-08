---
description: A ação PatchFiles consulta a tabela de patch para determinar quais patches devem ser aplicados. A ação PatchFiles também executa a aplicação de patches em byte dos arquivos.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Ação PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828436"
---
# <a name="patchfiles-action"></a>Ação PatchFiles

A ação PatchFiles consulta a [tabela de patch](patch-table.md) para determinar quais patches devem ser aplicados. A ação PatchFiles também executa a aplicação de patches em byte dos arquivos.

## <a name="sequence-restrictions"></a>Restrições de sequência

Se o arquivo a ser corrigido não estiver instalado, a ação PatchFiles deverá vir após a [ação InstallFiles](installfiles-action.md) que instala o arquivo. Os arquivos instalados anteriormente podem ser corrigidos em qualquer ponto na sequência de ação. A [ação DuplicateFiles](duplicatefiles-action.md) deve vir após a ação PatchFiles para impedir a duplicação da versão sem patch do arquivo.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador do arquivo com patch.                   |
| \[2\] | Identificador do diretório que contém o arquivo com patch. |
| \[3\] | Tamanho do patch em bytes.                       |



 

 

 



