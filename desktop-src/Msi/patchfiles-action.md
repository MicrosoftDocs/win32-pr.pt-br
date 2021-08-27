---
description: A ação PatchFiles consulta a tabela de patch para determinar quais patches devem ser aplicados. A ação PatchFiles também executa a aplicação de patches em byte dos arquivos.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Ação PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6186f150df1871e424b1dc6e4f466d148a1ce2ed51ffd9cd8170a1221e2f0b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082666"
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



 

 

 



