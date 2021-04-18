---
description: Este tópico descreve as diferenças entre as versões binárias da biblioteca do Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Qual versão da biblioteca deve ser referenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781556"
---
# <a name="which-library-version-to-reference"></a>Qual versão da biblioteca deve ser referenciada

Este tópico descreve as diferenças entre as versões binárias da biblioteca do Tablet PC.

## <a name="tablet-pc-library-versions"></a>Versões da biblioteca do Tablet PC

Os binários da biblioteca do Tablet PC (Microsoft.Ink.dll) foram atualizados no Windows Vista. Esses binários são chamados de "versão 6,0" para incide com a versão do Windows na qual estão sendo lançados.

A versão mais recente dos binários que são compatíveis com o Windows XP é conhecida como "versão 1,7".

O SDK do Windows pode ser instalado em computadores com vista e XP, e o SDK do Windows inclui as duas versões do Microsoft.Ink.dll.

Eles são instalados em:

1. % ProgramFiles% \\ Reference Assemblies \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll

2. % ProgramFiles% \\ Reference Assemblies \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll

Os binários da versão 6,0 são compatíveis apenas com o Windows Vista, e os aplicativos escritos neles só devem ser executados no Windows Vista.

Um aplicativo escrito em relação aos binários da versão 1,7 deve ser executado sem modificação quando instalado no Windows Vista.

 

 



