---
description: Um processo de duas etapas estende o modelo de transação do Windows Installer para os produtos que contêm Common Language Runtime assemblies. Isso permite que o instalador reverta instalações e remoções de assemblies malsucedidas.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reversão de assemblies no cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647054"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Reversão de assemblies no cache de assembly global

Um processo de duas etapas estende o modelo de transação do Windows Installer para os produtos que contêm Common Language Runtime assemblies. Isso permite que o instalador reverta instalações e remoções de assemblies malsucedidas.

Durante a primeira etapa, o Windows Installer usa a estrutura de Microsoft .NET para criar uma interface para cada assembly. O Windows Installer usa tantas interfaces quanto há assemblies sendo instalados. A confirmação de um assembly usando apenas uma dessas interfaces significa que o assembly está pronto para substituir qualquer assembly existente com o mesmo nome, mas ainda não o substitui. Se o usuário cancelar a instalação ou se houver um erro fatal de instalação, o Windows Installer ainda poderá reverter o assembly para seu estado anterior, liberando essas interfaces.

Depois que o Windows Installer concluir a instalação de todos os assemblies e componentes de Windows Installer, o instalador poderá iniciar a segunda etapa da instalação. A segunda etapa usa uma função separada para fazer a confirmação final de todos os novos assemblies de Common Language Runtime. Isso substitui todos os assemblies existentes com o mesmo nome.

 

 



