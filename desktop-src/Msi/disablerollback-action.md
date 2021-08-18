---
description: A ação DisableRollback desabilita a reversão para o restante da instalação.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Ação DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe500e3b810e5b06802e3a0face1da9b76441099a407882da08d5911a37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745366"
---
# <a name="disablerollback-action"></a>Ação DisableRollback

A ação DisableRollback desabilita a [reversão](rollback-installation.md) para o restante da instalação. A reversão é desabilitada somente para as ações que são sequenciadas após a ação DisableRollback nas tabelas de sequência. A reversão será desabilitada para toda a instalação se a ação DisableRollback for sequenciada antes da [ação InstallInitialize](installinitialize-action.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-message"></a>Mensagem ActionData

Não há nenhuma mensagem ActionData.

 

 



