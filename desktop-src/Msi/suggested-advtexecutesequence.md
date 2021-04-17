---
description: As sequências de ação sugeridas para uma tabela AdvtExecuteSequence básica em um banco de dados Windows Installer.
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: AdvtExecuteSequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a672579a174a0cc242ac503225d81976de60d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754342"
---
# <a name="suggested-advtexecutesequence"></a>AdvtExecuteSequence sugerido



| Ação                                                    | Condição | Sequência |
|-----------------------------------------------------------|-----------|----------|
| [CostInitialize](costinitialize-action.md)               |           | 800      |
| [CostFinalize](costfinalize-action.md)                   |           | 1000     |
| [InstallValidate](installvalidate-action.md)             |           | 1.400     |
| [InstallInitialize](installinitialize-action.md)         |           | 1500     |
| [Createatalhos](createshortcuts-action.md)             |           | 4500     |
| [RegisterClassInfo](registerclassinfo-action.md)         |           | 4600     |
| [RegisterExtensionInfo](registerextensioninfo-action.md) |           | 4700     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)       |           | 4800     |
| [RegisterMIMEInfo](registermimeinfo-action.md)           |           | 4900     |
| [PublishComponents](publishcomponents-action.md)         |           | 6200     |
| [PublishFeatures](publishfeatures-action.md)             |           | 6300     |
| [PublishProduct](publishproduct-action.md)               |           | 6400     |
| [InstallFinalize](installfinalize-action.md)             |           | 6600     |



 

 

 



