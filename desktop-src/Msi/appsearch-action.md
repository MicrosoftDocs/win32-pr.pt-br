---
description: A ação AppSearch usa assinaturas de arquivo para pesquisar versões existentes de produtos.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Ação AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169206"
---
# <a name="appsearch-action"></a>Ação AppSearch

A ação AppSearch usa assinaturas de arquivo para pesquisar versões existentes de produtos. A ação AppSearch pode usar essas informações para determinar onde as atualizações devem ser instaladas. A ação AppSearch também pode ser usada para definir uma propriedade para o valor existente de uma entrada de arquivo Registry ou. ini.

## <a name="sequence-restrictions"></a>Restrições de sequência

AppSearch deve ser criado na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md). O instalador impede que a ação AppSearch seja executada na sequência InstallExecuteSequence se a ação já tiver sido executada na sequência InstallUISequence.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação      |
|-------|---------------------------------|
| \[1\] | Propriedade que mantém o local do arquivo. |
| \[2\] | Assinatura de arquivo.                 |



 

## <a name="remarks"></a>Comentários

A ação AppSearch requer que a tabela de [assinatura](signature-table.md) esteja presente no pacote de instalação. As assinaturas de arquivo são listadas na tabela de assinatura. Uma assinatura que não está na tabela de assinatura denota um diretório e a ação define a propriedade como o caminho do diretório para essa assinatura.

A ação AppSearch pesquisa assinaturas de arquivo usando a tabela [CompLocator](complocator-table.md) primeiro, a tabela [RegLocator](reglocator-table.md) em seguida, a tabela [IniLocator](inilocator-table.md) e, por fim, a tabela [DrLocator](drlocator-table.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[AppSearch](appsearch-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



