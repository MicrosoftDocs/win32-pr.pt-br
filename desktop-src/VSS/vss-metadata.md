---
description: Os gravadores e os solicitantes mantêm as informações necessárias para uma operação de backup ou restauração em seus próprios documentos de metadados.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadados do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e69d0a40bbbce2d231573d187843c14bd83fea419a7024940d0fd618838500b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986576"
---
# <a name="vss-metadata"></a>Metadados do VSS

Os gravadores e os solicitantes mantêm as informações necessárias para uma operação de backup ou restauração em seus próprios documentos de metadados.

Esses documentos, o [*documento de metadados do gravador*](vssgloss-w.md) e o [*documento de componentes de backup*](vssgloss-b.md), respectivamente, são usados como base para comunicação e coordenação do gravador e do solicitante durante as atividades de backup e restauração.

Os metadados são representados em formato XML usando um esquema proprietário. Os metadados podem ser copiados em disco, fita ou em qualquer outro dispositivo de armazenamento em massa. Ele sempre deve ser salvo na mídia de backup durante uma operação de backup e precisará ser recuperado dessa mídia no decorrer de uma operação de restauração.

**Cuidado:** Os detalhes específicos do formato e do esquema são apenas para uso do sistema. Os desenvolvedores não devem tentar modificar ou usar diretamente a representação XML dos metadados.

Gravadores e solicitantes são fornecidos com uma variedade de métodos de consulta e definição para acessar e modificar os componentes de backup e os documentos de metadados do gravador:

-   [Trabalhando com o documento de metadados do gravador](working-with-the-writer-metadata-document.md)
-   [Trabalhando com o documento de componentes de backup](working-with-the-backup-components-document.md)
-   [Componentes de metadados do VSS](vss-metadata-components.md)

 

 



