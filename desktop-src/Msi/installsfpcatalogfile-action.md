---
description: A ação InstallSFPCatalogFile instala os catálogos usados pela proteção de arquivo do Windows me para Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Ação InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759656"
---
# <a name="installsfpcatalogfile-action"></a>Ação InstallSFPCatalogFile

A ação InstallSFPCatalogFile instala os catálogos usados pela proteção de arquivo do Windows me para Windows. InstallSFPCatalogFile consulta a [tabela de componentes](component-table.md), a [tabela de arquivos](file-table.md), a tabela [FileSFPCatalog](filesfpcatalog-table.md) e a [tabela SFPCatalog](sfpcatalog-table.md). Os catálogos são instalados se estiverem associados a um arquivo em um componente definido para instalação local ou se estiverem associados a um arquivo que está sendo reparado em um componente instalado localmente.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallSFPCatalogFile deve ser sequenciada antes de [InstallFiles](installfiles-action.md) e depois de [CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nome do catálogo que está sendo instalado.                          |
| \[2\] | Nome do catálogo no qual a instalação do catálogo depende. |



 

## <a name="remarks"></a>Comentários

Um catálogo que é dependente de outro catálogo instalado após o catálogo pai.

 

 



