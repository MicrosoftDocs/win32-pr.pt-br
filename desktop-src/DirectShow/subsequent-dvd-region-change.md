---
description: Alteração de região do DVD subsequente
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Alteração de região do DVD subsequente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6da91ff9fefb17480bbc502deb2fea80683e5861d32cfa4d4fa1a5cb22c2847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633286"
---
# <a name="subsequent-dvd-region-change"></a>Alteração de região do DVD subsequente

no Windows 2000 e posterior, o navegador de dvd invoca uma página de propriedades no dispositivo de unidade de DVD-ROM na Gerenciador de Dispositivos. Essa página de propriedades também é apresentada pelo aplicativo DVDPlay.exe quando uma região precisa ser alterada. A interface do usuário dessa página de propriedades é muito semelhante à do DVDRgn.exe e é regional no sistema operacional.

para unidades RPC1, os componentes do sistema operacional Windows gerenciam alterações de região. As unidades RPC2 mantêm a configuração de região em seu próprio hardware. Quando o número de alterações permitidas for esgotado em uma unidade RPC2, a unidade falhará na chamada para alterar a região e o componente de alteração de região no sistema operacional indicará que ao usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à alteração da região do DVD no Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



