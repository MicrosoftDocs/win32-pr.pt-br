---
description: O procedimento a seguir descreve um cenário para gerar uma transformação que oculta permanentemente um recurso.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Gerando uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011301"
---
# <a name="generating-a-transform"></a>Gerando uma transformação

O procedimento a seguir descreve um cenário para gerar uma transformação que oculta permanentemente um recurso.

**Para ocultar permanentemente um recurso de produto**

1.  Copie o pacote de instalação original.
2.  Altere a cópia definindo o valor da coluna de exibição na tabela de [recursos](feature-table.md) para zero. Isso especifica a ocultação do recurso.
3.  Crie uma transformação do pacote de instalação original para os novos pacotes de instalação chamando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Crie as informações de resumo na transformação chamando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

A transformação está pronta para ser aplicada durante a instalação. Para obter mais informações, consulte [aplicando transformações](applying-transforms.md).

 

 



