---
description: Para melhorar o desempenho, o acesso aos objetos da interface de dispositivo de gráficos (GDI) (como paletas, contextos de dispositivo, regiões e similares) não é serializado.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Vários threads e objetos GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782297"
---
# <a name="multiple-threads-and-gdi-objects"></a>Vários threads e objetos GDI

Para melhorar o desempenho, o acesso aos objetos da interface de dispositivo de gráficos (GDI) (como paletas, contextos de dispositivo, regiões e similares) não é serializado. Isso cria um perigo potencial para processos que têm vários threads compartilhando esses objetos. Por exemplo, se um thread excluir um objeto GDI enquanto outro thread o estiver usando, os resultados serão imprevisíveis. Esse perigo pode ser evitado simplesmente por não compartilhar objetos GDI. Se o compartilhamento for inevitável (ou desejável), o aplicativo deverá fornecer seus próprios mecanismos para sincronizar o acesso. Para obter mais informações sobre a sincronização de acesso, consulte [sincronizando a execução de vários threads](synchronizing-execution-of-multiple-threads.md).

 

 



