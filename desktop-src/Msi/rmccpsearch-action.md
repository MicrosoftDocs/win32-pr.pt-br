---
description: A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes que uma instalação de atualização seja executada.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Ação RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d18431a6806d055c824bf51331d6390a6f669100aa9a33db9665b9d7b37008c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625895"
---
# <a name="rmccpsearch-action"></a>Ação RMCCPSearch

A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes que uma instalação de atualização seja executada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RMCCPSearch deve ser baseada na tabela [InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md). O instalador impede que o RMCCPSearch seja executado na sequência InstallExecuteSequence se a ação já tiver sido executado na sequência InstallUISequence.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

A ação RMCCPSearch requer que a propriedade [**unidade \_ CCP**](ccp-drive.md) seja definida como o caminho raiz no volume removível que tem a instalação para qualquer um dos produtos qualificados. [](v-gly.md)

Cada assinatura de arquivo na tabela CCPSearch é pesquisada no caminho referenciado pela propriedade [**CCP \_ DRIVE**](ccp-drive.md) usando a [tabela DrLocator.](drlocator-table.md) A ausência da assinatura da tabela [Assinatura](signature-table.md) indica um diretório. Se qualquer assinatura for determinada como existente, a ação RMCCPSearch será encerrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



