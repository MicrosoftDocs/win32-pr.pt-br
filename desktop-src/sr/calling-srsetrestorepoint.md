---
title: Chamando SRSetRestorePoint
description: Um aplicativo pode criar um ponto de restauração antes de causar uma alteração significativa do sistema, como uma instalação, desinstalação ou atualização de recursos.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ee2fc64fc74dd9ceeff4856a6a63effe0667ff2bd837d7dc8ae521172a1c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592206"
---
# <a name="calling-srsetrestorepoint"></a>Chamando SRSetRestorePoint

Um aplicativo pode criar um ponto de restauração antes de causar uma alteração significativa do sistema, como uma instalação, desinstalação ou atualização de recursos.

Os instaladores devem criar um ponto de restauração logo antes da instalação chamando a função [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com o membro **dwEventType** da estrutura [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) definido como BEGIN \_ SYSTEM \_ CHANGE. Para notificar Restauração do Sistema que a instalação foi concluída, chame **SRSetRestorePoint** com **dwEventType** definido como END \_ SYSTEM \_ CHANGE.

Se o usuário cancelar a instalação do aplicativo, o instalador poderá remover o ponto de restauração criado quando a instalação foi iniciada. Remover o ponto de restauração é opcional e pode impedir que o usuário se recupere de alterações não intencional feitas pelo instalador durante o cancelamento. Se o instalador for remover um ponto de restauração, ele poderá chamar a função [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) ou chamar [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com **dwRestorePointType** definido como CANCELLED \_ OPERATION, **dwEventType** definido como END SYSTEM CHANGE e \_ \_ **llSequenceNumber** definido como o valor retornado pela chamada inicial para **SRSetRestorePoint**.

**Windows 8: **

Uma nova chave do Registro permite que os desenvolvedores de aplicativos alterem a frequência de criação do ponto de restauração.

Os aplicativos devem criar essa chave para usá-la porque ela não será preexistência no sistema. O seguinte será aplicado por padrão se a chave não existir. Se um aplicativo chamar a função **SRSetRestorePoint** para criar um ponto de restauração, o Windows ignorará a criação desse novo ponto de restauração se algum ponto de restauração tiver sido criado nas últimas 24 horas. Restauração do Sistema define o membro **IISequenceNumber** da estrutura [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) como o número de sequência para o ponto de restauração criado anteriormente no dia e define o valor do membro **nStatus** como **ERROR \_ SUCCESS.** A **função SRSetRestorePoint** retorna **TRUE.**

Os desenvolvedores podem escrever aplicativos que criam o valor **DWORD** **SystemRestorePointCreationFrequency** na chave do Registro **HKLM \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ SystemRestore**. O valor dessa chave do Registro pode alterar a frequência de criação do ponto de restauração. O valor dessa chave do Registro pode alterar a frequência de criação do ponto de restauração.

Se o aplicativo chamar **SRSetRestorePoint** para criar um ponto de restauração e o valor da chave do Registro for 0, a restauração do sistema não ignorará a criação do novo ponto de restauração.

Se o aplicativo chamar **SRSetRestorePoint** para criar um ponto de restauração e o valor da chave do Registro for o inteiro N, a restauração do sistema ignorará a criação de um novo ponto de restauração se algum ponto de restauração tiver sido criado nos N minutos anteriores.

**Windows 8: **

Restauração do Sistema em execução Windows 8 monitora arquivos no volume de inicialização relevantes apenas para restauração do sistema. Instantâneos do volume de inicialização criado pelo Restauração do Sistema em execução no Windows 8 poderão ser excluídos se o instantâneo for subsequentemente exposto por uma versão anterior do Windows. Observe que, embora haja apenas um volume do sistema, há um volume de inicialização para cada sistema operacional em um sistema de várias inicializações.

Os desenvolvedores podem escrever aplicativos que criam o valor **DWORD** **ScopeSnapshots** na chave do Registro **HKLM \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ SystemRestore**. Se esse valor de chave do Registro for 0, Restauração do Sistema criará instantâneos do volume de inicialização da mesma maneira que nas versões anteriores do Windows. Se esse valor for excluído, Restauração do Sistema em execução no Windows 8 retomará a criação de instantâneos que monitoram arquivos no volume de inicialização relevantes apenas para restauração do sistema.

Para ver um exemplo, consulte [Usando Restauração do Sistema](using-system-restore.md).

 

 




