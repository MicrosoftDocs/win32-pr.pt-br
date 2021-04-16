---
description: Antes que um aplicativo possa adicionar dados ao registro, ele deve criar ou abrir uma chave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Abrindo, criando e fechando chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751057"
---
# <a name="opening-creating-and-closing-keys"></a>Abrindo, criando e fechando chaves

Antes que um aplicativo possa adicionar dados ao registro, ele deve criar ou abrir uma chave. Para criar ou abrir uma chave, um aplicativo sempre se refere à chave como uma subchave de uma chave aberta no momento. As seguintes chaves predefinidas são sempre abertas: **HKEY \_ local \_ Machine**, **HKEY \_ classes \_ root**, **HKEY \_ Users** e **HKEY \_ Current \_ User**. Um aplicativo usa a função [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) para abrir uma chave e a função [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) para criar uma chave. Uma árvore do registro pode ter 512 níveis de profundidade. Você pode criar até 32 níveis por vez por meio de uma única chamada à API do registro.

Um aplicativo pode usar a função [**falha RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) para fechar uma chave e gravar os dados que ela contém no registro. O **falha RegCloseKey** não grava necessariamente os dados no registro antes de retornar; pode levar até vários segundos para que o cache seja liberado para o disco rígido. Se um aplicativo precisar gravar dados de registro explicitamente no disco rígido, ele poderá usar a função [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) . O **RegFlushKey**, no entanto, usa muitos recursos do sistema e deve ser chamado somente quando absolutamente necessário.

 

 



