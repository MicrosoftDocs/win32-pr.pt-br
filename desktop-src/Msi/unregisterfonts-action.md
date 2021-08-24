---
description: A ação UnregisterFonts remove informações de registro sobre as fontes instaladas do sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Ação UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786996"
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

 

 



