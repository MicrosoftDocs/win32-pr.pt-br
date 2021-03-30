---
title: Chamando SRSetRestorePoint
description: Um aplicativo pode criar um ponto de restauração antes de causar uma alteração significativa no sistema, como uma instalação, desinstalação ou atualização de recursos.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b877c4fe73bcedad363bb4c9cc770a9638550dbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636729"
---
# <a name="calling-srsetrestorepoint"></a>Chamando SRSetRestorePoint

Um aplicativo pode criar um ponto de restauração antes de causar uma alteração significativa no sistema, como uma instalação, desinstalação ou atualização de recursos.

Os instaladores devem criar um ponto de restauração logo antes da instalação chamando a função [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com o membro **DwEventType** da estrutura [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) definida para iniciar a \_ alteração do sistema \_ . Para notificar a restauração do sistema de que a instalação foi concluída, chame **SRSetRestorePoint** com **DWEVENTTYPE** definido como finalizar \_ alteração do sistema \_ .

Se o usuário cancelar a instalação do aplicativo, o instalador poderá remover o ponto de restauração criado quando a instalação começou. A remoção do ponto de restauração é opcional e pode impedir que o usuário se recupere de alterações não intencionais feitas pelo instalador durante o cancelamento. Se o instalador for remover um ponto de restauração, ele poderá chamar a função [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) ou chamar [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com **dwRestorePointType** definido para a operação cancelada \_ , **dwEventType** definido como finalizar \_ alteração do sistema \_ e **llSequenceNumber** definido como o valor retornado pela chamada inicial para **SRSetRestorePoint**.

**Windows 8:  **

Uma nova chave do Registro permite que os desenvolvedores de aplicativos alterem a frequência da criação do ponto de restauração.

Os aplicativos devem criar essa chave para usá-la porque ela não existirá no sistema. O seguinte será aplicado por padrão se a chave não existir. Se um aplicativo chamar a função **SRSetRestorePoint** para criar um ponto de restauração, o Windows ignorará a criação desse novo ponto de restauração se quaisquer pontos de restauração tiverem sido criados nas últimas 24 horas. A restauração do sistema define o membro **IISequenceNumber** da estrutura [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) para o número de sequência do ponto de restauração criado anteriormente no dia e define o valor do membro **NStatus** para **o \_ êxito do erro**. A função **SRSetRestorePoint** retorna **true**.

Os desenvolvedores podem escrever aplicativos que criam o valor **DWORD** **SystemRestorePointCreationFrequency** na chave do registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. O valor dessa chave do registro pode alterar a frequência da criação do ponto de restauração. O valor dessa chave do registro pode alterar a frequência da criação do ponto de restauração.

Se o aplicativo chamar **SRSetRestorePoint** para criar um ponto de restauração e o valor da chave do registro for 0, a restauração do sistema não ignorará a criação do novo ponto de restauração.

Se o aplicativo chamar **SRSetRestorePoint** para criar um ponto de restauração e o valor da chave do registro for o inteiro N, a restauração do sistema ignorará a criação de um novo ponto de restauração se qualquer ponto de restauração tiver sido criado nos N minutos anteriores.

**Windows 8:  **

A restauração do sistema em execução no Windows 8 monitora arquivos no volume de inicialização que são relevantes somente para restauração do sistema. Os instantâneos do volume de inicialização criados pela restauração do sistema em execução no Windows 8 poderão ser excluídos se o instantâneo for posteriormente exposto por uma versão anterior do Windows. Observe que, embora haja apenas um volume do sistema, há um volume de inicialização para cada sistema operacional em um sistema de várias inicializações.

Os desenvolvedores podem escrever aplicativos que criam o valor **DWORD** **ScopeSnapshots** na chave do registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. Se esse valor de chave do registro for 0, a restauração do sistema criará instantâneos do volume de inicialização da mesma maneira que nas versões anteriores do Windows. Se esse valor for excluído, a restauração do sistema em execução no Windows 8 retomará a criação de instantâneos que monitoram arquivos no volume de inicialização que são relevantes somente para restauração do sistema.

Para obter um exemplo, consulte [usando a restauração do sistema](using-system-restore.md).

 

 




