---
description: a ação InstallSFPCatalogFile instala os catálogos usados pelo Windows Me para proteção de arquivo do Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Ação InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f3992a64e5e3150759fdbc2c8221e6bd8672a2c75e72343280fb3e552f3cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787006"
---
# <a name="installsfpcatalogfile-action"></a>Ação InstallSFPCatalogFile

a ação InstallSFPCatalogFile instala os catálogos usados pelo Windows Me para proteção de arquivo do Windows. InstallSFPCatalogFile consulta a [tabela de componentes](component-table.md), a [tabela de arquivos](file-table.md), a tabela [FileSFPCatalog](filesfpcatalog-table.md) e a [tabela SFPCatalog](sfpcatalog-table.md). Os catálogos são instalados se estiverem associados a um arquivo em um componente definido para instalação local ou se estiverem associados a um arquivo que está sendo reparado em um componente instalado localmente.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallSFPCatalogFile deve ser sequenciada antes de [InstallFiles](installfiles-action.md) e depois de [CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nome do catálogo que está sendo instalado.                          |
| \[2\] | Nome do catálogo no qual a instalação do catálogo depende. |



 

## <a name="remarks"></a>Comentários

Um catálogo que é dependente de outro catálogo instalado após o catálogo pai.

 

 



