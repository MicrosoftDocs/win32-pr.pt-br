---
description: As sequências de ação sugeridas para uma tabela InstalUISequence básica em um banco de dados Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751626"
---
# <a name="suggested-installuisequence"></a>InstallUISequence sugerido



| Ação                                          | Condição                                                                                                  | Sequência |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| FatalErrorDlg                                   |                                                                                                            | -3       |
| UserExitDlg                                     |                                                                                                            | -2       |
| ExitDlg                                         |                                                                                                            | -1       |
| [LaunchConditions](launchconditions-action.md) |                                                                                                            | 100      |
| PrepareDlg                                      |                                                                                                            | 140      |
| [AppSearch](appsearch-action.md)               |                                                                                                            | 400      |
| [CCPSearch](ccpsearch-action.md)               | Não [ **instalado**](installed.md)                                                                         | 500      |
| [RMCCPSearch](rmccpsearch-action.md)           | Não [ **instalado**](installed.md)                                                                         | 600      |
| [CostInitialize](costinitialize-action.md)     |                                                                                                            | 800      |
| [Custo de](filecost-action.md)                 |                                                                                                            | 900      |
| [CostFinalize](costfinalize-action.md)         |                                                                                                            | 1000     |
| WelcomeDlg                                      | Não [ **instalado**](installed.md)                                                                         | 1230     |
| ResumeDlg                                       | [**Instalado**](installed.md) E ( [**retomar**](resume.md) ou [**selecionável**](preselected.md))       | 1240     |
| MaintenanceWelcomeDlg                           | [**Instalado**](installed.md) E não [**retomar**](resume.md) e não [**selecionável**](preselected.md) | 1250     |
| ProgressDlg                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 



