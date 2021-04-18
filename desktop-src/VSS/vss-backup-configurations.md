---
description: Há vários tipos de backup com suporte em Convenção&\# 8212; incremental, diferencial e completa&\# 8212; que o VSS reconhece, bem como uma configuração de backup peculiar para o VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurações de backup do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781078"
---
# <a name="vss-backup-configurations"></a>Configurações de backup do VSS

Há vários tipos de backup com suporte de Convenção – incremental, diferencial e completo – que o VSS reconhece, bem como uma configuração de backup peculiar para o VSS.

Ao definir uma configuração de backup, um solicitante e os gravadores em um sistema indicam como os dados serão gravados em um dispositivo de armazenamento, como o mecanismo de cópia de sombra será implantado e quais informações precisam ser salvas. A interação entre escritores e solicitantes é determinada pelo tipo de backup que um solicitante deseja executar e os tipos (ou esquemas) aos quais cada gravador pode dar suporte:

-   [Estado de backup do VSS](vss-backup-state.md)
-   [Suporte ao esquema de backup do gravador](writer-backup-schema-support.md)
-   [Suporte a esquema de nível de arquivo](file-level-schema-support.md)

 

 



