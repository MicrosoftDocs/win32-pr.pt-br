---
description: Uma transformação é uma coleção de alterações aplicadas a uma instalação. Aplicando uma transformação a um pacote de instalação base, o instalador pode adicionar ou substituir dados no banco de dados de instalação. O instalador só pode aplicar as transformação durante uma instalação.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Sobre as transformaçãos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635430fb5e75b658880d5c5670219cae950502421c2b188af0381fd60ad3d48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013264"
---
# <a name="about-transforms"></a>Sobre as transformaçãos

Uma transformação é uma coleção de alterações aplicadas a uma instalação. Aplicando uma transformação a um pacote de instalação base, o instalador pode adicionar ou substituir dados no banco de dados de instalação. O instalador só pode aplicar as transformação durante uma instalação.

O instalador registra uma lista de transformaçãos exigidas pelo produto durante a instalação. O instalador deve aplicar essas transformação ao pacote de instalação do produto ao configurar ou instalar o produto. Se uma transformação listada não estiver disponível e se a resiliência de origem de transformação não puder restaurá-la, a instalação falhará.

Uma transformação pode modificar informações que estão em qualquer tabela persistente no banco [de dados do instalador](installer-database.md). Uma transformação também pode adicionar ou remover tabelas persistentes no banco de dados do instalador. As transformaçãos não podem modificar nenhuma parte de um pacote de instalação que não está em uma tabela de banco de dados, como informações no fluxo de informações de resumo [,](summary-information-stream.md)informações em substorages ou arquivos em gabinetes inseridos.

As transformaçãos têm um fluxo de informações resumidos que pode conter condições de validação e condições de erro. As condições de erro e validação de transformação podem ser adicionadas às informações resumidas usando a [**função MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) As condições de validação controlam se o instalador pode aplicar a transformação a um determinado banco de dados de instalação. A validação da transformação pode ser condicionada nos valores das propriedades [**UpgradeCode**](upgradecode.md), [**ProductCode,**](productcode.md) [**ProductVersion**](productversion.md) e [**ProductLanguage**](productlanguage.md) especificadas na transformação e aquelas no banco de dados de instalação. As condições de erro de transformação controlam quais erros são suprimidos quando a transformação é aplicada. As condições de erro incluídas na transformação são substituídos pelas condições de erro especificadas usando os métodos [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) e [**ApplyTransform.**](database-applytransform.md)

> [!Note]  
> As transformares de personalização típicas não têm condições de validação ou validam em [**relação ao ProductCode.**](productcode.md) As transformares armazenadas em [pacotes de patch](patch-packages.md) geralmente têm condições de validação estritas para garantir que a transformação correta seja aplicada ao destino do patch.

 

Há três tipos de Windows instalador:

-   [Transformações inseridas](embedded-transforms.md)
-   [Transformaçãos protegidas](secured-transforms.md)
-   [Transformações não asseguradas](unsecured-transforms.md)

 

 



