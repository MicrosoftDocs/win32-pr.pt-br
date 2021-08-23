---
description: As ações personalizadas não devem chamar a função SRSetRestorePoint porque isso pode resultar na escrita de um ponto de entrada de restauração no meio de uma instalação Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Definindo um ponto de restauração de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628576"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Definindo um ponto de restauração de uma ação personalizada

As ações personalizadas não devem chamar a função [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) porque isso pode resultar na escrita de um ponto de entrada de restauração no meio de uma instalação Windows Instalador.

Para obter mais informações, [consulte Restauração do Sistema e o instalador Windows .](system-restore-points-and-the-windows-installer.md)

 

 
