---
description: Os carimbos de data/hora normalmente são incluídos quando um arquivo é assinado usando SignTool com a opção -t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Adicionando carimbos de data/hora a arquivos assinados anteriormente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880226"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Adicionando carimbos de data/hora a arquivos assinados anteriormente

Os carimbos de data/hora normalmente são incluídos quando um arquivo é assinado usando SignTool com a **opção -t.** Além disso, carimbos de data/hora podem ser adicionados a arquivos que foram assinados sem um carimbo de data/hora. O comando a seguir adiciona um carimbo de data/hora a um arquivo assinado anteriormente:

**signtool timestamp -t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> O arquivo com carimbo de data/hora deve ter sido assinado anteriormente.

 

Para obter mais informações sobre o SignTool, consulte [SignTool](signtool.md).

 

 



