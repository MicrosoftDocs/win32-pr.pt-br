---
description: A ação RegisterFonts registra as fontes instaladas com o sistema. Essa ação mapeia o nome da fonte na coluna FontTitle da tabela Font para o caminho do arquivo de fonte instalado.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Ação RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2588dc1e2fd332521d43a7cefc4aae0378a63747166154730e0b832a9bf3835b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339706"
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

 

 



