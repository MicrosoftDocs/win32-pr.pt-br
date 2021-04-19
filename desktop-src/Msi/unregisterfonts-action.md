---
description: A ação UnregisterFonts remove informações de registro sobre as fontes instaladas do sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Ação UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812904"
---
# <a name="unregisterfonts-action"></a>Ação UnregisterFonts

A ação UnregisterFonts remove informações de registro sobre as fontes instaladas do sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [RemoveFiles](removefiles-action.md) deve ser chamada após UnregisterFonts.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Arquivo de fonte.                 |



 

## <a name="remarks"></a>Comentários

A ação UnregisterFonts será executada se o arquivo especificado na coluna arquivo \_ da tabela de [fontes](font-table.md) pertencer a um componente que está sendo desinstalado.

 

 



