---
description: A ação INSTALL é uma ação de nível superior chamada para instalar ou remover componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Ação INSTALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5f648084b7386465f6bb59dd6b523cb51489e4cb83677c0b5cb47fe845be42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810996"
---
# <a name="install-action"></a>Ação INSTALL

A ação INSTALL é uma ação de nível superior chamada para instalar ou remover componentes. Essa ação consulta a Tabela [InstallUISequence](installuisequence-table.md) e [a Tabela InstallExecuteSequence](installexecutesequence-table.md) para a ação a ser executada, a condição para execução da ação e o local da ação na sequência:

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

A ação INSTALL não é chamada de dentro da sequência de tabela de ação, ela é passada para o instalador do Windows quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado ou o executável de linha de comando Msiexec.exe é chamado com a opção de linha de comando '**/i**' ou quando qualquer função do instalador é chamada que pode executar uma tarefa de instalação, como [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)ou [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



