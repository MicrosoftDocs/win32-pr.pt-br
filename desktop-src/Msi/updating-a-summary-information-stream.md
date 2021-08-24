---
description: O valor da Propriedade Resumo do Número de Revisão no fluxo de informações de resumo deve ser alterado para um novo valor exclusivo ao localizador de um banco de dados, pois o banco de dados de instalação está sendo alterado. Consulte Códigos de pacote.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Atualizando um fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d95e6a0cf09af5d4a024f707c0694d89def47abf8f731f394c55a11232bc07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039276"
---
# <a name="updating-a-summary-information-stream"></a>Atualizando um fluxo de informações de resumo

O valor da Propriedade [**Resumo**](revision-number-summary.md) [](summary-information-stream.md) do Número de Revisão no fluxo de informações de resumo deve ser alterado para um novo valor exclusivo ao localizador de um banco de dados, pois o banco de dados de instalação está sendo alterado. Consulte [Códigos de pacote](package-codes.md).

O valor da Propriedade [**resumo do**](template-summary.md) modelo no fluxo de informações de resumo deve ser alterado para o LANGID (identificador de idioma numérico) do novo idioma.

Se as cadeias de caracteres de texto descritivas no fluxo de informações resumidas são localizadas para o novo idioma, a Propriedade [**de**](codepage-summary.md) Resumo da Página de Código deve ser definida como a página de código correta para o novo idioma.

Você pode modificar o fluxo de informações resumidas do pacote localizado pelo mesmo procedimento que em [Adicionando informações resumidas.](adding-summary-information.md) Um exemplo que demonstra o uso dos métodos de informações de resumo do banco de dados também é fornecido no SDK do Windows Installer como o utilitário WiSumInf.vbs. Para obter mais informações sobre WiSumInf.vbs, consulte [Gerenciar informações resumidas.](manage-summary-information.md)

[Continuar](adding-localized-resources.md)

 

 



