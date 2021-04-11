---
description: O Windows Installer determina se deve permitir a remoção de um assembly de Common Language Runtime com base em uma lista de clientes que ele mantém independentemente do assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Remoção de assemblies do cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169521"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Remoção de assemblies do cache de assembly global

O Windows Installer determina se deve permitir a remoção de um assembly de Common Language Runtime com base em uma lista de clientes que ele mantém independentemente do assembly. O Windows Installer mantém um bit PIN para representar Windows Installer clientes do assembly. O instalador fixa o assembly para o primeiro cliente Windows Installer e o desafixa quando o último cliente Windows Installer é removido. O assembly mantém um bit de PIN para cada cliente de um assembly.

O Windows Installer não é diretamente responsável pela remoção física de assemblies de Common Language Runtime do computador. O instalador desafixa o assembly quando o último cliente de Windows Installer é removido. Se o Windows Installer for o último cliente do assembly, o Common Language Runtime fornecerá a opção de forçar uma limpeza síncrona do assembly. O processo de limpeza é atômico e não há nenhuma provisão para uma "reversão" neste ponto. Toda a desanexação de assemblies de Common Language Runtime deve ocorrer depois que o usuário tiver a oportunidade de cancelar a instalação ou remoção.

 

 



