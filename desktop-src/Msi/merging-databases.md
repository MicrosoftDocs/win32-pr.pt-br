---
description: Você pode usar o instalador para adicionar as informações de um banco de dados em outro banco de dados executando uma mesclagem.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Mesclando bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2931bb624037f2f909b99cfeb19a64fcb4abef689fe988a308d35766f50b1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628702"
---
# <a name="merging-databases"></a>Mesclando bancos de dados

Você pode usar o instalador para adicionar as informações de um banco de dados em outro banco de dados executando uma mesclagem. [Mesclagens e transformações](merges-and-transforms.md) funcionam em um banco de dados inteiro e uma mesclagem combina dois bancos de dados em um. As mesclagens são úteis para as equipes de desenvolvimento porque permitem que o banco de dados de instalação de aplicativo grande seja dividido em partes menores e, em seguida, recombinadas no banco de dados de instalação completo mais tarde.

**Para mesclar vários bancos de dados de componentes em um único banco de dados completo**

1.  Desenvolva os bancos de dados de componentes parciais separadamente.
2.  Mescle cada banco de dados de componente no banco de dados do produto principal chamando a função [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .

 

 



