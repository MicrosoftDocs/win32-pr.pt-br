---
description: O código-fonte para uma ação personalizada de exemplo chamada Launch, que atende às especificações de exemplo, é fornecido pelo SDK do Windows Installer como o arquivo tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Criando a ação personalizada de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921488"
---
# <a name="authoring-the-launch-custom-action"></a>Criando a ação personalizada de inicialização

O código-fonte para uma ação personalizada de exemplo chamada Launch, que atende às especificações de exemplo, é fornecido pelo SDK do Windows Installer como o arquivo tutorial. cpp. Essa ação personalizada faz uso de [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para formatar uma cadeia de caracteres que contém propriedades. A propriedade \[ \# FileKey é \] resolvida para o caminho completo do arquivo HTML. Use o arquivo de origem para criar o arquivo Tutorial.dll. O ponto de entrada para essa DLL é LaunchTutorial.

A inicialização da ação personalizada de exemplo chama uma DLL escrita em C++ e é gerada a partir de um fluxo binário temporário. As ações personalizadas desse tipo incluem as constantes de tipo base msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData, que fornecem um tipo numérico de base igual a 1. Consulte [tipo de ação personalizada 1](custom-action-type-1.md). Como as especificações exigem que a instalação continue se a ação personalizada falhar, a inicialização também incluirá a constante opcional **msidbCustomActionTypeContinue**, que é 64. Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md). O tipo numérico total de inicialização é 65.

Continue a [Adicionar Launch às tabelas CustomAction e binary](adding-launch-to-the-customaction-and-binary-tables.md).

 

 



