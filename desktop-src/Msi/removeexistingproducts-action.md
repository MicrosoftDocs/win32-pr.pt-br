---
description: A ação RemoveExistingProducts passa pelos códigos de produto listados na coluna Actionproperty da tabela de atualização e remove os produtos em sequência invocando instalações simultâneas.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Ação RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756720"
---
# <a name="removeexistingproducts-action"></a>Ação RemoveExistingProducts

A ação RemoveExistingProducts passa pelos códigos de produto listados na coluna Actionproperty da tabela de [atualização](upgrade-table.md) e remove os produtos em sequência invocando instalações simultâneas. Para cada instalação simultânea, o instalador define a propriedade [**ProductCode**](productcode.md) para o código do produto e define a propriedade [**Remove**](remove.md) como o valor no campo remove da tabela de atualização. Se o campo remover estiver em branco, seu valor padrão será todos e o instalador removerá o produto inteiro.

O instalador executa apenas a ação RemoveExistingProducts na primeira vez que instala um produto. Ele não executa a ação durante uma instalação ou desinstalação de [manutenção](maintenance-installation.md) .

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RemoveExistingProducts deve ser agendada na sequência de ações em um dos locais a seguir.

-   Entre a [ação InstallValidate](installvalidate-action.md) e a [ação InstallInitialize](installinitialize-action.md). Nesse caso, o instalador remove totalmente os aplicativos antigos antes de instalar os novos aplicativos. Esse é um posicionamento ineficiente para a ação porque todos os arquivos reutilizados precisam ser copiados novamente.
-   Após a [ação InstallInitialize](installinitialize-action.md) e antes de qualquer ação que gere o script de execução.
-   Entre a [ação InstallExecute](installexecute-action.md), ou a [ação InstallExecuteAgain](installexecuteagain-action.md), e a [ação InstallFinalize](installfinalize-action.md). Geralmente, as três últimas ações são agendadas logo após uma outra: InstallExecute, RemoveExistingProducts e InstallFinalize. Nesse caso, os arquivos atualizados são instalados primeiro e, em seguida, os arquivos antigos são removidos. No entanto, se a remoção do aplicativo antigo falhar, o instalador reverterá a remoção do aplicativo antigo e a instalação do novo aplicativo.
-   Após a [ação InstallFinalize](installfinalize-action.md). Esse é o posicionamento mais eficiente para a ação. Nesse caso, o instalador atualiza os arquivos antes de remover os aplicativos antigos. Somente os arquivos que estão sendo atualizados são instalados durante a instalação. Se a remoção do aplicativo antigo falhar, o instalador apenas reverterá a desinstalação do aplicativo antigo.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Produto removido.           |



 

## <a name="remarks"></a>Comentários

Windows Installer define a propriedade [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) quando ela executa essa ação.

 

 



