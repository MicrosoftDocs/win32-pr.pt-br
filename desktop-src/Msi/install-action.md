---
description: A ação de instalação é uma ação de nível superior chamada para instalar ou remover componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Ação de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010856"
---
# <a name="install-action"></a>Ação de instalação

A ação de instalação é uma ação de nível superior chamada para instalar ou remover componentes. Essa ação consulta a [tabela InstallUISequence](installuisequence-table.md) e a [tabela InstallExecuteSequence](installexecutesequence-table.md) para que a ação seja executada, a condição para execução da ação e o lugar da ação na sequência:

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação de instalação não é chamada de dentro da sequência da tabela de ações, ela é passada para Windows Installer quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado ou o executável de linha de comando Msiexec.exe é chamado com a opção de linha de comando '**/i**' ou quando qualquer função do instalador é chamada que pode executar uma tarefa de instalação, como [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)ou [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



