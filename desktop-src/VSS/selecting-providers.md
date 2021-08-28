---
description: Um solicitante deve selecionar um provedor específico somente se ele tiver algumas informações sobre os provedores disponíveis.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selecionando provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2451f172a569a23ba4799c16f8598ade4e6fb011f051b7ba7d948c7a366f22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124496"
---
# <a name="selecting-providers"></a>Selecionando provedores

Um solicitante deve selecionar um provedor específico somente se ele tiver algumas informações sobre os provedores disponíveis.

Como esse geralmente não será o caso, é recomendável que um solicitante fornecer GUID NULL como uma ID de provedor para \_ [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), que permite que o sistema escolha um provedor de acordo com o seguinte algoritmo:

1.  Se um provedor de hardware que dá suporte ao volume determinado estiver disponível, ele será selecionado.
2.  Se nenhum provedor de hardware estiver disponível, se qualquer provedor de software específico para o volume determinado estiver disponível, ele será selecionado.
3.  Se nenhum provedor de hardware e nenhum provedor de software específico para os volumes estiver disponível, o provedor do sistema será selecionado.

No entanto, um solicitante pode obter informações sobre provedores disponíveis usando [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query). Com essas informações e somente se o aplicativo de backup tiver uma boa compreensão dos vários provedores, um solicitante poderá fornecer uma ID de provedor válida para [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Observe que todos os volumes não precisam ter o mesmo provedor.

 

 



