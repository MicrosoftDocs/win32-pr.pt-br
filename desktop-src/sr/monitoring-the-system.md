---
title: Monitorando o sistema
description: Monitorando o sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363619"
---
# <a name="monitoring-the-system"></a>Monitorando o sistema

A restauração do sistema no Windows Vista e posterior salva uma cópia do volume ao gerar um ponto de restauração. A restauração do sistema requer um mínimo de 300 MB de espaço livre em disco na unidade do sistema na instalação.

A restauração do sistema no Windows XP monitora um conjunto principal de arquivos do sistema e do aplicativo, arquivando os Estados desses arquivos antes que as alterações do sistema sejam feitas. A restauração do sistema também salva um instantâneo completo do registro e alguns arquivos de sistema dinâmicos. A restauração do sistema requer um mínimo de 200 MB de espaço livre em disco na unidade do sistema na instalação. Quando a quantidade de espaço livre em disco cai abaixo de 50 MB em qualquer unidade, a restauração do sistema muda para o modo de espera e para a criação de pontos de restauração. Todos os pontos de restauração são excluídos nesse momento. A restauração do sistema reativa e retoma a criação de pontos de restauração assim que 200 MB de espaço em disco estão livres na unidade do sistema. Os arquivos monitorados ou excluídos do monitoramento são especificados no arquivo% windir% \\ System32 \\ restore \\Filelist.xml. Para obter mais informações, consulte [extensões de nome de arquivo monitorado](monitored-file-extensions.md).

 

 




