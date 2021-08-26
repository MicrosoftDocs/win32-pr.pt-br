---
description: O código-fonte de uma ação personalizada de exemplo chamada Launch, que atende às especificações de exemplo, é fornecido pelo SDK do Windows Installer como o arquivo Tutorial.cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Como iniciar a ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536f22c95d871ab502518a0619efad5ae70cb348cdf75163fc50309b440f6393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045266"
---
# <a name="authoring-the-launch-custom-action"></a>Como iniciar a ação personalizada

O código-fonte de uma ação personalizada de exemplo chamada Launch, que atende às especificações de exemplo, é fornecido pelo SDK do Windows Installer como o arquivo Tutorial.cpp. Essa ação personalizada usa [**MsiFormatRecord para**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) formatar uma cadeia de caracteres que contém propriedades. A propriedade \[ \# FileKey \] é resolvida para o caminho completo do arquivo HTML. Use o arquivo de origem para criar o arquivo Tutorial.dll. O ponto de entrada para essa DLL é LaunchTutorial.

A ação personalizada de exemplo Iniciar chama uma DLL escrita em C++ e é gerada de um fluxo binário temporário. As ações personalizadas desse tipo incluem as constantes de tipo base msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData, que dão um tipo numérico base igual a 1. Consulte [Tipo de ação personalizada 1.](custom-action-type-1.md) Como as especificações exigem que a instalação continue se a ação personalizada falhar, Iniciar também inclui a constante opcional **msidbCustomActionTypeContinue,** que é 64. Consulte [Opções de processamento de retorno de ação personalizada.](custom-action-return-processing-options.md) O tipo numérico total de Launch é 65.

Continue [adicionando Launch às tabelas CustomAction e Binary](adding-launch-to-the-customaction-and-binary-tables.md).

 

 



