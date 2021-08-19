---
title: Fechando um dispositivo
description: Fechando um dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f81ddaf42ef5509b55271159b8e36ac56584b92734a6b04e5b555041596530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498076"
---
# <a name="closing-a-device"></a>Fechando um dispositivo

O comando [**fechar**](close.md) ([**MCI \_ Close**](mci-close.md)) libera o acesso a um dispositivo ou arquivo. O MCI libera um dispositivo quando todas as tarefas que usam um dispositivo o fecham. Para ajudar o MCI a gerenciar os dispositivos, seu aplicativo deve fechar cada dispositivo ou arquivo quando terminar de usá-lo.

Quando você fecha um dispositivo MCI externo que usa sua própria mídia em vez de arquivos (como áudio de CD), o driver deixa o dispositivo em seu modo atual de operação. Portanto, se você fechar um dispositivo de áudio de CD que está sendo executado, mesmo que o driver de dispositivo seja liberado da memória, o dispositivo de áudio de CD continuará a ser reproduzido até atingir o final de seu conteúdo.

> [!Note]  
> fechar um aplicativo com dispositivos MCI abertos pode impedir que outros aplicativos usem esses dispositivos até que Windows seja reiniciado.

 

 

 




