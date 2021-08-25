---
description: Depois de selecionar o ICEs apropriado para validação, um desenvolvedor deve coletar as ações personalizadas em um banco de dados ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Criando um banco de dados ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e078517f8942454320e3f743d7379bbfeb22a7c44afe635a8276568a56c27f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926986"
---
# <a name="building-an-ice-database"></a>Criando um banco de dados ICE

Depois de selecionar o [ICES](internal-consistency-evaluators-ices.md) apropriado para validação, um desenvolvedor deve coletar as ações personalizadas em um banco de dados Ice. Um arquivo. Cub é um banco de dados .msi padrão que contém apenas ICEs e suas tabelas necessárias. Um arquivo. Cub não pode ser instalado e usado somente para armazenar e fornecer acesso a ações personalizadas do ICE.

Um arquivo. Cub contém as tabelas de banco de dados a seguir.



| Tabela                                  | Descrição                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binary](binary-table.md)             | Os arquivos de script, DLLs e EXEs das ações alfandegárias do ICE que são referenciadas na tabela CustomAction.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Cada registro nessa tabela corresponde a uma ação personalizada de ICE incluída no arquivo. cub.                                                                                                                                                                                   |
| \_ICESequence                          | Esta tabela lista as ações de Alfândegas do ICE incluídas no arquivo. Cub em sua sequência de execução. As ações personalizadas do ICE listadas nesta tabela são executadas chamando [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)ou individualmente executadas usando [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). |
| [\_Validação](-validation-table.md)  | Esta tabela contém as entradas de arquivo. Cub que devem ser mescladas na \_ tabela de validação.                                                                                                                                                                               |
| \_Especial                              | Todas as tabelas de processamento especial exigidas por ações personalizadas específicas do ICE devem ser incluídas no arquivo. cub. O nome dessas tabelas deve ter um sublinhado à esquerda.                                                                                                        |



 

Consulte o [arquivo. Cub de exemplo](sample--cub-file.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma ICE](building-an-ice.md)
</dt> </dl>

 

 



