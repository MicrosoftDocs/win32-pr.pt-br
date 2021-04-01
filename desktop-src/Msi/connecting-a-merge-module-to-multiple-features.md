---
description: O método Connect do objeto de mesclagem pode ser usado para conectar um módulo a um recurso adicional que foi mesclado ao banco de dados ou que será mesclado no banco de dados. O recurso deve existir antes de chamar este método.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Conectando um módulo de mesclagem a vários recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829352"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Conectando um módulo de mesclagem a vários recursos

O método [**Connect**](merge-connect.md) do [objeto de mesclagem](merge-object.md) pode ser usado para conectar um módulo a um recurso adicional que foi mesclado ao banco de dados ou que será mesclado no banco de dados. O recurso deve existir antes de chamar este método.

Um módulo de mesclagem nunca deve entregar um componente que contém arquivos do sistema ao recurso principal de um aplicativo, pois isso pode fazer com que o instalador valide e repare o aplicativo sempre que o arquivo do sistema for usado. Um arquivo. msi destinado a aceitar componentes de um módulo de mesclagem deve ser criado para que qualquer componente que contenha arquivos do sistema pertença apenas a recursos separados do recurso principal do aplicativo.

Se o pacote usar um módulo de mesclagem que contém arquivos do sistema que vinculam todos os componentes do módulo de mesclagem ao recurso principal do aplicativo, uma tentativa de usar o arquivo do sistema poderá disparar o instalador para tentar reparar o recurso principal do aplicativo. Se o recurso principal não puder ser reparado, a instalação poderá falhar.

 

 



