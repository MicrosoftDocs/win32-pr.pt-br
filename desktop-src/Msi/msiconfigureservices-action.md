---
description: A ação MsiConfigureServices configura um serviço para o sistema. Essa ação consulta as tabelas MsiServiceConfig e MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Ação MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750607"
---
# <a name="msiconfigureservices-action"></a>Ação MsiConfigureServices

A ação MsiConfigureServices configura um serviço para o sistema. Essa ação consulta as tabelas [MsiServiceConfig](msiserviceconfig-table.md) e [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Essa ação está disponível a partir do Windows Installer 5,0.

> [!IMPORTANT]
>
> Os serviços do Windows fornecem a capacidade de executar automaticamente ações predefinidas em resposta a uma falha em um serviço. Para dar suporte à configuração dessas **ações de recuperação** programaticamente quando um serviço falha, o [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) foi adicionado ao msi na versão MSI 5,0. No entanto, essa funcionalidade não está funcionando conforme o esperado.
>
> Para solucionar esse problema, um desenvolvedor de aplicativos deve usar a funcionalidade de **ação personalizada** no MSI para executar **sc.exe** e definir as **Opções de recuperação** adequadamente.

 

## <a name="sequence-restrictions"></a>Restrições de sequência

Essa ação padrão deve ser usada na sequência a seguir.

[Pararservices](stopservices-action.md)

[Excluirservices](deleteservices-action.md)

Qualquer uma das seguintes ações: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) ações.

[Instalarservices](installservices-action.md)

MsiConfigureServices

[Iniciarservices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para instalar serviços ou que o aplicativo faça parte de uma instalação gerenciada.

 

 



