---
description: Os autores de pacote devem garantir que os nomes de quaisquer tabelas, propriedades ou ações personalizadas definidas em seu pacote não entrem em conflito com os nomes de tabelas, propriedades ou ações padrão que são nativas para o Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Nomeando tabelas, propriedades e ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827871"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Nomeando tabelas, propriedades e ações personalizadas

Os autores de pacote devem garantir que os nomes de quaisquer tabelas, propriedades ou ações personalizadas definidas em seu pacote não entrem em conflito com os nomes de tabelas, propriedades ou ações padrão que são nativas para o Windows Installer.

Os autores de pacote devem aderir às seguintes diretrizes para nomes de ações, propriedades ou tabelas personalizadas.

-   Crie nomes para tabelas, propriedades ou ações personalizadas que tenham um prefixo que identifique seu aplicativo.
-   Nunca use um nome com MSI como o prefixo. A partir do Windows Installer 2,0, todas as novas propriedades, ações e tabelas de Windows Installer nativas recebem nomes prefixados pelo MSI. Esse prefixo não diferencia maiúsculas de minúsculas, por exemplo, MsiNewInternalTable. Como o prefixo não diferencia maiúsculas de minúsculas, os autores devem evitar todos os casos do prefixo msi.

Para obter mais informações, consulte [nomes de tabela](table-names.md).

 

 



