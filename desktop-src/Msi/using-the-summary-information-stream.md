---
description: Esta seção descreve quais funções na API Windows Installer podem chamar as propriedades do fluxo de informações de resumo. Para obter mais informações sobre o fluxo de informações de resumo e como ele funciona com bancos de dados, consulte sobre o fluxo de informações de resumo.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Usando o fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921779"
---
# <a name="using-the-summary-information-stream"></a>Usando o fluxo de informações de resumo

Esta seção descreve quais funções na API Windows Installer podem chamar as propriedades do fluxo de informações de resumo. Para obter mais informações sobre o fluxo de informações de resumo e como ele funciona com bancos de dados, consulte [sobre o fluxo de informações de resumo](about-the-summary-information-stream.md).

-   É importante lembrar que o instalador contém diferentes tipos de bancos de dados e algumas propriedades do fluxo de informações resumidas têm significados diferentes com bancos de dados diferentes. Para obter mais informações, consulte [Summary Property Descriptions](summary-property-descriptions.md).
-   Quando um banco de dados é aberto como a saída de outro banco de dados, o fluxo de informações de resumo do banco de dados de saída é, na verdade, um espelho somente leitura do banco de dados original e, portanto, não pode ser alterado. Além disso, ele não será persistido com o banco de dados. Para criar ou modificar as informações de resumo do banco de dados de saída, ele deve ser fechado e aberto novamente.

As etapas a seguir descrevem como usar as funções de fluxo de informações de Resumo:

**Para usar as propriedades do fluxo de informações de resumo**

1.  Obtenha um identificador para o banco de dados que contém o fluxo de informações de resumo chamando a função [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) .
2.  Chame a função [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) para obter o número de propriedades existentes.
3.  Chame a função [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) para exibir uma única propriedade de informações de resumo.
4.  Chamar a função [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) para definir uma única propriedade
5.  Chame a função [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) para salvar a propriedade de informações de resumo.
6.  Chame a função [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) para criar as informações de resumo para uma transformação existente.

[Orca.exe](orca-exe.md) e [Msiinfo.exe](msiinfo-exe.md) são ferramentas que podem ser usadas para editar ou exibir o fluxo de informações de Resumo de um banco de dados. Essas ferramentas estão disponíveis apenas nos [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

O fluxo de informações de resumo também pode ser acessado usando os seguintes métodos e propriedades da [interface de automação](automation-interface.md)de Windows Installer.

-   [**SummaryInfo. Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo.PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo. Persist**](summaryinfo-persist.md)
-   [**Installer. SummaryInformation**](installer-summaryinformation.md)
-   [**Database. SummaryInformation**](database-summaryinformation.md)
-   [**Database. CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

O arquivo VBScript WiSumInf.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este script de exemplo pode ser usado para gerenciar o fluxo de informações de Resumo de um pacote de Windows Installer. Para obter mais informações sobre WiSumInf.vbs, consulte [gerenciar informações de resumo](manage-summary-information.md).

 

 



