---
description: Há vários tipos de backup com suporte em Convenção&\# 8212; incremental, diferencial e completa&\# 8212; que o VSS reconhece, bem como uma configuração de backup peculiar para o VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurações de backup do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8552bc379be4fc2bf7301043355a1a4417a59154ea15c36061b9cfd13c5d209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056334"
---
# <a name="vss-backup-configurations"></a>Configurações de backup do VSS

Há vários tipos de backup com suporte de Convenção – incremental, diferencial e completo – que o VSS reconhece, bem como uma configuração de backup peculiar para o VSS.

Ao definir uma configuração de backup, um solicitante e os gravadores em um sistema indicam como os dados serão gravados em um dispositivo de armazenamento, como o mecanismo de cópia de sombra será implantado e quais informações precisam ser salvas. A interação entre escritores e solicitantes é determinada pelo tipo de backup que um solicitante deseja executar e os tipos (ou esquemas) aos quais cada gravador pode dar suporte:

-   [Estado de backup do VSS](vss-backup-state.md)
-   [Suporte ao esquema de backup do gravador](writer-backup-schema-support.md)
-   [Suporte a esquema de nível de arquivo](file-level-schema-support.md)

 

 



