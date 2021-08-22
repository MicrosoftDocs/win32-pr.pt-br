---
description: Este tópico descreve as diferenças entre as versões binárias da biblioteca de computadores Tablet.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Qual versão da biblioteca deve ser referenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899866dd11bbe72f9476ee3b645ed4e5612fe7043dae38675bd206e81562ca68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589276"
---
# <a name="which-library-version-to-reference"></a>Qual versão da biblioteca deve ser referenciada

Este tópico descreve as diferenças entre as versões binárias da biblioteca de computadores Tablet.

## <a name="tablet-pc-library-versions"></a>Versões da biblioteca de TABLET PC

Os binários da biblioteca de computadores tablets (Microsoft.Ink.dll) foram atualizados no Windows Vista. Esses binários são chamados de "versão 6.0" para fazer a co-entrada com a versão do Windows na qual eles estão sendo liberados.

A versão mais recente dos binários compatíveis com o Windows XP é conhecida como "versão 1.7".

O Windows SDK pode ser instalado em máquinas Vista e XP, e o SDK do Windows inclui as duas versões do Microsoft.Ink.dll.

Eles são instalados em:

1. %programfiles% \\ Assemblies de referência \\ microsoft tablet pc \\ \\ v1.7 \\Microsoft.Ink.dll

2. %programfiles% \\ Assemblies de referência \\ microsoft tablet pc \\ \\ v6.0 \\Microsoft.Ink.dll

Os binários da versão 6.0 são compatíveis apenas com o Windows Vista e os aplicativos escritos neles só devem ser executados no Windows Vista.

Um aplicativo escrito nos binários da versão 1.7 deve ser executado sem modificação quando instalado no Windows Vista.

 

 



