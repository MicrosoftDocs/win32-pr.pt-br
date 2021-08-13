---
description: Um processo de duas etapas estende o Windows de transação do instalador para produtos que contêm assemblies do Common Language Runtime. Isso permite que o instalador reverter instalações e remoções malsucedida de assemblies.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reação de assemblies no cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625821"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Reação de assemblies no cache de assembly global

Um processo de duas etapas estende o Windows de transação do instalador para produtos que contêm assemblies do Common Language Runtime. Isso permite que o instalador reverter instalações e remoções malsucedida de assemblies.

Durante a primeira etapa, o Windows instalador usa o Microsoft .NET Framework para criar uma interface para cada assembly. O Windows instalador usa tantas interfaces quanto assemblies que estão sendo instalados. A confirmação de um assembly usando uma dessas interfaces significa apenas que o assembly está pronto para substituir qualquer assembly existente pelo mesmo nome, ele ainda não o substitui. Se o usuário cancelar a instalação ou se houver um erro fatal de instalação, o instalador do Windows ainda poderá reverter o assembly para seu estado anterior liberando essas interfaces.

Depois que Windows instalador do Windows instalar todos os assemblies, o instalador poderá iniciar a segunda etapa da instalação. A segunda etapa usa uma função separada para fazer a confirmação final de todos os novos assemblies do Common Language Runtime. Isso substitui todos os assemblies existentes pelo mesmo nome.

 

 



