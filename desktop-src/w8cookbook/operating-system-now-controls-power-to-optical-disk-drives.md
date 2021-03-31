---
title: O sistema operacional agora controla a energia em unidades de disco ópticos
description: O sistema operacional agora controla a energia em unidades de disco ópticos
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641958"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>O sistema operacional agora controla a energia em unidades de disco ópticos

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

Nas versões anteriores do Windows, a energia para a unidade óptica não era gerenciada quando a unidade óptica não estava em uso. Agora, se não houver nenhuma mídia presente na unidade de disco óptico (ímpar), o sistema operacional desligará a potência para a unidade óptica. Esse recurso é chamado de energia ímpar (ZPODD). O recurso é aplicável somente a unidades ópticas que usam um conector Slimline SATA (Serial Advanced Technology Attachment).

## <a name="manifestation"></a>Manifestação

Não encontramos nenhum impacto negativo desse novo comportamento; no entanto, você deve estar ciente dela, pois isso pode resultar em um comportamento inesperado do software de gravação de mídia.

## <a name="mitigation"></a>Atenuação

Para reverter para o status do Always on, desative essa funcionalidade no registro. O caminho absoluto para o valor do registro é:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Seu tipo é DWORD (32 bits) e, se seu valor for 0, ZPODD será desabilitado; Se for qualquer outro valor, ZPODD será habilitado.

## <a name="tests"></a>Testes

Teste seu software de gravação de mídia para qualquer anomalia que ocorra devido a esse novo recurso. [Informe a Microsoft](mailto:OptIssue@microsoft.com) sobre os problemas encontrados com esse novo recurso.

 

 




