---
description: Reenumerando e atualizando
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Reenumerando e atualizando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763184"
---
# <a name="reenumerating-and-refreshing"></a>Reenumerando e atualizando

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

A operação de reenumeração descobre os dispositivos recentemente conectados e recentemente desconectados. A operação de atualização atualiza as informações de configuração dos dispositivos existentes.

**Para reenumerar objetos de provedor de software**

-   Chame o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) . Esse método descobre todos os discos recentemente conectados e desconectados e unidades de CD-ROM e garante que todos os discos tenham o proprietário adequado. O VDS possui discos brutos ou discos com falhas; o provedor básico possui discos básicos; e o provedor dinâmico possui discos dinâmicos. Essa operação pode envolver a verificação de barramentos de subsistema internos e a espera de tempos limite.

**Para reenumerar e atualizar objetos do provedor de software**

-   Chame o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) e, em seguida, chame o método [**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) . Além de descobrir discos e unidades de CD-ROM recentemente conectados e desconectados, essa combinação de métodos atualiza todas as informações de disco, volume e Plex no cache do VDS para discos que não foram conectados ou desconectados recentemente. Chame somente **Atualizar** para atualizar as informações de propriedade de objetos existentes no cache. Essa operação pode envolver a verificação de barramentos de subsistema internos e a espera de tempos limite. Observe que o VDS atualiza o cache automaticamente sempre que ocorre uma alteração que dispara uma notificação. Além disso, chamar a **atualização** em resposta a uma notificação do VDS pode fazer com que um loop interminável de notificações seja enviado. Por esses motivos, a **atualização** deve ser chamada somente quando parece que o cache não está sendo atualizado corretamente.

**Para reenumerar subsistemas de hardware**

-   Chame o método [**IVdsHwProvider:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) . Dependendo do provedor, essa operação pode envolver o envio de pacotes de rede e a espera de tempos limite, a verificação de barramentos SCSI e a espera de tempos limite e assim por diante.

**Para reenumerar objetos de subsistema de hardware**

-   Chame o método [**IVdsSubSystem:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) para inventariar os objetos (normalmente unidades) no subsistema. Dependendo do subsistema, essa operação pode envolver a verificação de barramentos de subsistema internos e a espera de tempos limite.

**Para atualizar subsistemas de hardware e objetos de subsistema**

-   Chame o método [**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) para atualizar o cache VDS de informações sobre subsistemas existentes que são gerenciados por provedores de hardware VDS. Observe que o VDS atualiza o cache automaticamente sempre que ocorre uma alteração que dispara uma notificação. Além disso, chamar a [**atualização**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) em resposta a uma notificação do VDS pode fazer com que um loop interminável de notificações seja enviado. Por esses motivos, a **atualização** deve ser chamada somente quando parece que o cache não está sendo atualizado corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService:: atualizar**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider:: atualizar**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
