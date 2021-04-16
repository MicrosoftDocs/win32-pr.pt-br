---
description: A ação RegisterFonts registra as fontes instaladas com o sistema. Essa ação mapeia o nome da fonte na coluna FontTitle da tabela Font para o caminho do arquivo de fonte instalado.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Ação RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747949"
---
# <a name="registerfonts-action"></a>Ação RegisterFonts

A ação RegisterFonts registra as fontes instaladas com o sistema. Essa ação mapeia o nome da fonte na coluna FontTitle da [tabela Font](font-table.md) para o caminho do arquivo de fonte instalado.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [InstallFiles](installfiles-action.md) deve ser chamada antes de chamar a ação RegisterFonts.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Arquivo de fonte.                 |



 

## <a name="remarks"></a>Comentários

A ação RegisterFonts será executada se o arquivo especificado na coluna arquivo \_ da tabela de [fontes](font-table.md) pertencer a um componente que está sendo instalado.

 

 



