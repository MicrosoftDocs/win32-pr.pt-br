---
description: Os carimbos de data e hora normalmente são incluídos quando um arquivo é assinado usando SignTool com a opção-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Adicionando carimbos de data/hora a arquivos assinados anteriormente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105756380"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Adicionando carimbos de data/hora a arquivos assinados anteriormente

Os carimbos de data e hora normalmente são incluídos quando um arquivo é assinado usando SignTool com a opção **-t** . Além disso, carimbos de data/hora podem ser adicionados a arquivos que foram assinados sem um carimbo de data/hora. O comando a seguir adiciona um carimbo de data/hora a um arquivo assinado anteriormente:

**carimbo de data/hora de SignTool-t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> O carimbo de data/hora do arquivo deve ter sido assinado anteriormente.

 

Para obter mais informações sobre SignTool, consulte [SignTool](signtool.md).

 

 



