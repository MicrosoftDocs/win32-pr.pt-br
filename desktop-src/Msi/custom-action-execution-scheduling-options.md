---
description: Como uma ação personalizada pode ser agendada na interface do usuário e executar tabelas de sequência e pode ser executada no processo do serviço ou do cliente, uma ação personalizada pode potencialmente ser executada várias vezes.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opções de agendamento de execução de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755086"
---
# <a name="custom-action-execution-scheduling-options"></a>Opções de agendamento de execução de ação personalizada

Como uma ação personalizada pode ser agendada na interface do usuário e executar tabelas de sequência e pode ser executada no processo do serviço ou do cliente, uma ação personalizada pode potencialmente ser executada várias vezes.

Observe que o instalador:

-   Executa ações em uma tabela de sequência imediatamente por padrão.
-   Não executará uma ação se o campo expressão condicional da tabela de sequência for avaliado como false.
-   Processa a tabela de sequências da interface do usuário no processo do cliente se o nível da interface dos usuários internos estiver definido como o modo de interface de usuário completo (consulte [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obter uma descrição dos níveis de IU).
-   É um serviço registrado por padrão ao usar o Windows 2000 e, nesse caso, a tabela de sequências de execução é processada no serviço do instalador.

Você pode usar os seguintes sinalizadores de opção para controlar várias execuções imediatas de ações personalizadas. Para definir uma opção, adicione o valor nessa tabela ao valor no campo tipo da [tabela CustomAction](customaction-table.md). Nenhum dos sinalizadores a seguir deve ser usado com [ações personalizadas de execução adiada](deferred-execution-custom-actions.md).

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>os
</dt> <dd>

Hexadecimal: 0x00000000

Decimal: 0

Sempre executar. A ação pode ser executada duas vezes se estiver presente em ambas as tabelas de sequência.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Hexadecimal: 0x00000100

Decimal: 256

Execute não mais de uma vez se estiver presente em ambas as tabelas de sequência. Sempre ignora a ação na sequência de execução se a sequência da interface do usuário tiver sido executada. Nenhum efeito na sequência da interface do usuário. A ação não precisa estar presente ou ser executada na sequência da interface do usuário para ser ignorada na sequência de execução. Não afetado pelo registro do serviço de instalação.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Hexadecimal: 0x00000200

Decimal: 512

Execute uma vez por processo se estiver em ambas as tabelas de sequência. Ignora a ação na sequência de execução se a sequência da interface do usuário foi executada no mesmo processo, por exemplo, ambas são executadas no processo do cliente. Usado para impedir que as ações que modificam o estado da sessão, como dados de propriedade e de Database, sejam executadas duas vezes.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Hexadecimal: 0x00000300

Decimal: 768

Execute somente se estiver executando no cliente após a execução da sequência da interface do usuário. A ação será executada somente se a sequência de execução for executada no cliente após a sequência de interface do usuário. Pode ser usado para fornecer ou/ou lógica, ou para suprimir o processamento relacionado à interface do usuário, se já tiver feito para a sessão do cliente.

</dd> </dl>

Observe que, para executar uma ação personalizada durante dois modos de execução diferentes, crie duas entradas na [tabela CustomAction](customaction-table.md) . Por exemplo, para ter uma ação personalizada que chama uma DLL (biblioteca de vínculo dinâmico) do C/C++ ( [tipo de ação personalizada 1](custom-action-type-1.md)) quando o modo for MSIRUNMODE \_ agendado e MSIRUNMODE \_ Rollback, coloque duas entradas na tabela CustomAction que chamam a mesma DLL, mas que têm tipos numéricos diferentes. Inclua o código que chama [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para determinar quando executar qual ação personalizada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ação personalizada](custom-action-reference.md)
</dt> <dt>

[Sobre ações personalizadas](about-custom-actions.md)
</dt> <dt>

[Usando ações personalizadas](using-custom-actions.md)
</dt> </dl>

 

 



