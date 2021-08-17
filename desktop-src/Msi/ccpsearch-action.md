---
description: A ação CCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Ação CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201af22dd557541825dcf2c47f06e7cf67cd8785fa85e0b78a28c25a570ffc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145689"
---
# <a name="ccpsearch-action"></a>Ação CCPSearch

A ação CCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação CCPSearch deve ser criada na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md). O instalador impede que a ação CCPSearch seja executada na sequência InstallExecuteSequence se a ação já tiver sido executada na sequência InstallUISequence. A ação CCPSearch deve vir antes da ação [RMCCPSearch](rmccpsearch-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação CCPSearch procura por assinaturas de arquivo listadas na tabela CCPSearch no sistema usando as seguintes tabelas em ordem: assinatura, CompLocator, RegLocator, IniLocator e DrLocator.

Se alguma assinatura for determinada para existir, a **propriedade \_ êxito do CCP** será definida como 1 e a ação CCPSearch terminará.

A ausência da assinatura da tabela de assinatura denota um diretório.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CCPSearch](ccpsearch-table.md)
</dt> <dt>

[Signature](signature-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



