---
description: O valor da propriedade Resumo do número de revisão no fluxo de informações de resumo deve ser alterado para um valor novo e exclusivo ao localizar um banco de dados, pois o banco de dados de instalação está sendo alterado. Consulte códigos de pacote.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Atualizando um fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370777"
---
# <a name="updating-a-summary-information-stream"></a>Atualizando um fluxo de informações de resumo

O valor da propriedade [**Resumo do número de revisão**](revision-number-summary.md) no [fluxo de informações de resumo](summary-information-stream.md) deve ser alterado para um valor novo e exclusivo ao localizar um banco de dados, pois o banco de dados de instalação está sendo alterado. Consulte [códigos de pacote](package-codes.md).

O valor da propriedade de [**Resumo do modelo**](template-summary.md) no fluxo de informações de resumo deve ser alterado para o identificador de idioma numérico (LangID) do novo idioma.

Se as cadeias de caracteres de texto descritivos no fluxo de informações de resumo forem localizadas para o novo idioma, a propriedade de [**Resumo CodePage**](codepage-summary.md) deverá ser definida como a página de código correta para o novo idioma.

Você pode modificar o fluxo de informações resumidas do pacote localizado pelo mesmo procedimento que a [adição de informações resumidas](adding-summary-information.md). Um exemplo que demonstra o uso dos métodos de informações de resumo do banco de dados também é fornecido no SDK do Windows Installer como o WiSumInf.vbs do utilitário. Para obter mais informações sobre WiSumInf.vbs, consulte [gerenciar informações de resumo](manage-summary-information.md).

[Continuar](adding-localized-resources.md)

 

 



