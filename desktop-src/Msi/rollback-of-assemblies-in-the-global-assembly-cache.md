---
description: um processo de duas etapas estende o modelo de transação do Windows Installer para os produtos que contêm Common Language Runtime assemblies. Isso permite que o instalador reverta instalações e remoções de assemblies malsucedidas.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reversão de assemblies no cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625821"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Reversão de assemblies no cache de assembly global

um processo de duas etapas estende o modelo de transação do Windows Installer para os produtos que contêm Common Language Runtime assemblies. Isso permite que o instalador reverta instalações e remoções de assemblies malsucedidas.

durante a primeira etapa, o Windows Installer usa o Microsoft .NET Framework para criar uma interface para cada assembly. o Windows Installer usa tantas interfaces quanto há assemblies sendo instalados. A confirmação de um assembly usando apenas uma dessas interfaces significa que o assembly está pronto para substituir qualquer assembly existente com o mesmo nome, mas ainda não o substitui. se o usuário cancelar a instalação ou se houver um erro fatal de instalação, o Windows Installer ainda poderá reverter o assembly para seu estado anterior, liberando essas interfaces.

depois que o Windows Installer concluir a instalação de todos os assemblies e componentes de Windows Installer, o instalador poderá iniciar a segunda etapa da instalação. A segunda etapa usa uma função separada para fazer a confirmação final de todos os novos assemblies de Common Language Runtime. Isso substitui todos os assemblies existentes com o mesmo nome.

 

 



