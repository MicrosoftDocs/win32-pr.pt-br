---
description: Msival2.exe é um utilitário de linha de comando que pode executar um conjunto de avaliadores de consistência internos-ICEs.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ed1228413d5b2fab0dfab79ea4546a9d15e74c8c62e9b1ca9751699f469854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943873"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe é um utilitário de linha de comando que pode executar um conjunto de [avaliadores de consistência internos-ICES](internal-consistency-evaluators-ices.md).

essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Para obter mais informações sobre ICEs e o arquivo CUB, consulte [usando avaliadores de consistência internos](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Syntax

**Msival2** *{Database} {arquivo Cub} \[ -f \] \[ -l {logfile} \] \[ -i {ID do Ice} \[ : {ID do Ice}. \] \] ..*

## <a name="command-line-options"></a>Opções de linha de comando

Msival2.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço.



| Opção | Descrição                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtre todas as mensagens informativas dos resultados exibidos. Todos os outros tipos de mensagens são exibidos.                                                                                                                                                                                              |
| -i     | Execute apenas o ICEs listado na linha de comando na ordem especificada. Cada ação personalizada de ICE deve ser listada como aparece na [tabela CustomAction](customaction-table.md) do arquivo Cub. Se essa opção for omitida, a ferramenta executará o conjunto padrão de ICEs especificado pelo autor do arquivo CUB. |
| -l     | Gravar resultados no arquivo especificado. O arquivo ainda não deve existir. Se o arquivo existir, ele não será substituído.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> <dt>

[Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



