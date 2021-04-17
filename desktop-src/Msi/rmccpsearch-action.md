---
description: A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Ação RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789767"
---
# <a name="rmccpsearch-action"></a>Ação RMCCPSearch

A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RMCCPSearch deve ser criada na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md). O instalador impede que o RMCCPSearch seja executado na sequência InstallExecuteSequence se a ação já tiver sido executada na sequência InstallUISequence.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação RMCCPSearch requer que a propriedade da [**\_ unidade CCP**](ccp-drive.md) seja definida como o caminho raiz no [*volume*](v-gly.md) removível que tem a instalação para qualquer um dos produtos qualificados.

Cada assinatura de arquivo na tabela CCPSearch é pesquisada sob o caminho referido pela propriedade da [**\_ unidade CCP**](ccp-drive.md) usando a tabela [DrLocator](drlocator-table.md) . A ausência da assinatura da tabela de [assinatura](signature-table.md) denota um diretório. Se alguma assinatura for determinada para existir, a ação RMCCPSearch será encerrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



