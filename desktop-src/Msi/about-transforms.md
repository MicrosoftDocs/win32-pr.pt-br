---
description: Uma transformação é uma coleção de alterações aplicadas a uma instalação do. Aplicando uma transformação a um pacote de instalação base, o instalador pode adicionar ou substituir dados no banco de dado de instalação. O instalador só pode aplicar transformações durante uma instalação.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Sobre transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169219"
---
# <a name="about-transforms"></a>Sobre transformações

Uma transformação é uma coleção de alterações aplicadas a uma instalação do. Aplicando uma transformação a um pacote de instalação base, o instalador pode adicionar ou substituir dados no banco de dado de instalação. O instalador só pode aplicar transformações durante uma instalação.

O instalador registra uma lista de transformações exigidas pelo produto durante a instalação. O instalador deve aplicar essas transformações ao pacote de instalação do produto ao configurar ou instalar o produto. Se uma transformação listada não estiver disponível e se a resiliência da origem da transformação não puder restaurá-la, a instalação falhará.

Uma transformação pode modificar as informações que estão em qualquer tabela persistente no [banco de dados do instalador](installer-database.md). Uma transformação também pode adicionar ou remover tabelas persistentes no banco de dados do instalador. As transformações não podem modificar nenhuma parte de um pacote de instalação que não esteja em uma tabela de banco de dados, como informações no [fluxo de informações resumidas](summary-information-stream.md), informações em subarmazenamentos ou arquivos em gabinetes incorporados.

As transformações têm um fluxo de informações resumido que pode conter condições de validação e condições de erro. A validação de transformação e as condições de erro podem ser adicionadas às informações de resumo usando a função [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . As condições de validação controlam se o instalador pode aplicar a transformação a um determinado banco de dados de instalação. A validação da transformação pode ser condicionada nos valores das propriedades [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) e [**ProductLanguage**](productlanguage.md) especificadas na transformação e aquelas no banco de dados de instalação. As condições de erro de transformação controlam quais erros são suprimidos quando a transformação é aplicada. As condições de erro incluídas na transformação são substituídas pelas condições de erro especificadas usando os métodos [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) e [**ApplyTransform**](database-applytransform.md) .

> [!Note]  
> As transformações de personalização típicas não têm condições de validação ou são validadas em relação ao [**ProductCode**](productcode.md). As transformações armazenadas nos [pacotes de patch](patch-packages.md) geralmente têm condições de validação estritas para garantir que a transformação correta seja aplicada ao destino do patch.

 

Há três tipos de transformações de Windows Installer:

-   [Transformações inseridas](embedded-transforms.md)
-   [Transformações protegidas](secured-transforms.md)
-   [Transformações não seguras](unsecured-transforms.md)

 

 



