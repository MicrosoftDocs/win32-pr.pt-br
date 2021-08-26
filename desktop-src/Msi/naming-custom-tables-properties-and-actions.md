---
description: os autores de pacote devem garantir que os nomes de quaisquer tabelas, propriedades ou ações personalizadas definidas em seu pacote não entrem em conflito com os nomes de tabelas, propriedades ou ações padrão que são nativas para o Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Nomeando tabelas, propriedades e ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd26ab08bcada936bdcb9c87d10cb060c697689cec8978a1eae0d25ac5c0a2d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105076"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Nomeando tabelas, propriedades e ações personalizadas

os autores de pacote devem garantir que os nomes de quaisquer tabelas, propriedades ou ações personalizadas definidas em seu pacote não entrem em conflito com os nomes de tabelas, propriedades ou ações padrão que são nativas para o Windows Installer.

Os autores de pacote devem aderir às seguintes diretrizes para nomes de ações, propriedades ou tabelas personalizadas.

-   Crie nomes para tabelas, propriedades ou ações personalizadas que tenham um prefixo que identifique seu aplicativo.
-   Nunca use um nome com MSI como o prefixo. a partir do Windows Installer 2,0, todas as novas propriedades, ações e tabelas de Windows Installer nativas recebem nomes prefixados pelo Msi. Esse prefixo não diferencia maiúsculas de minúsculas, por exemplo, MsiNewInternalTable. Como o prefixo não diferencia maiúsculas de minúsculas, os autores devem evitar todos os casos do prefixo msi.

Para obter mais informações, consulte [nomes de tabela](table-names.md).

 

 



