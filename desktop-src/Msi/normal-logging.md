---
description: O instalador registra erros e eventos em seu próprio log de erros.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Log normal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd1abeb4f110603bcc596cb7981ea65c7d9820d8054adc7533c4f85de2d8bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828536"
---
# <a name="normal-logging"></a>Log normal

O instalador registra erros e eventos em seu próprio log de erros. O tipo de log que é executado pelo instalador é determinado pela configuração do modo de log. O registro em log está habilitado e o modo pode ser definido usando os seguintes métodos:

-   O modo de log de uma instalação iniciada na linha de comando pode ser especificado usando a opção/L das [Opções de linha de comando](command-line-options.md). Se o modo de log não for especificado usando a opção de linha de comando/L, o modo de log padrão será usado.
-   O modo de log de um processo de instalação pode ser especificado programaticamente usando a função [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) ou o método [**EnableLog**](installer-enablelog.md) . Se o modo de log não for especificado usando a função **MsiEnableLog** ou o método **EnableLog** , o modo de log padrão será usado.
-   O modo de log padrão de um determinado pacote de instalação pode ser especificado definindo a propriedade [**MsiLogging**](msilogging.md) na [tabela de propriedades](property-table.md) do pacote. essa propriedade está disponível a partir do Windows Installer 4,0.
-   Se a propriedade [**MsiLogging**](msilogging.md) estiver presente na [tabela de propriedades](property-table.md), o modo de log padrão do pacote poderá ser modificado alterando o valor usando uma transformação de banco de [dados](database-transforms.md). O modo de log padrão não pode ser alterado usando [pacotes de patches](patch-packages.md) (um arquivo. msp).
-   Se a propriedade [**MsiLogging**](msilogging.md) não tiver sido definida, o modo de log padrão para todos os usuários do computador poderá ser especificado usando a política de [registro em log](logging.md) .
-   Se a propriedade [**MsiLogging**](msilogging.md) tiver sido definida, o modo de log padrão para todos os usuários do computador poderá ser especificado definindo a política de [DisableLoggingFromPackage](disableloggingfrompackage.md) e a política de [registro em log](logging.md) .
-   Se o modo de log não tiver sido especificado pela opção/L, [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), [**MsiLogging**](msilogging.md) ou pela política de [registro em log](logging.md) , o modo de log padrão do pacote será o mesmo modo obtido como a definição da propriedade **MsiLogging** como ' iwearmo '.

 

 



