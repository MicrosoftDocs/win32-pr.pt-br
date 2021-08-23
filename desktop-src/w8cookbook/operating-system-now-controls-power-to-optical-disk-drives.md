---
title: O sistema operacional agora controla a potência das unidades de disco óptico
description: O sistema operacional agora controla a potência das unidades de disco óptico
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc43ad47f6a9468c2850627f267d433bfa346d059231d5daa91e860d5a793aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593796"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>O sistema operacional agora controla a potência das unidades de disco óptico

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

Nas versões anteriores do Windows, a energia para a unidade óptica não era gerenciada quando a unidade óptica não estava em uso. Agora, se não houver nenhuma mídia presente na unidade de disco óptico (ODD), o sistema operacional desligará a energia para a unidade óptica. Esse recurso é chamado de ZPODD (zero power ODD). O recurso é aplicável somente a unidades ópticas que usam um conector SATA (Serial Advanced Technology Attachment).

## <a name="manifestation"></a>Manifestação

Não encontramos nenhum impacto negativo desse novo comportamento; no entanto, você deve estar ciente disso, pois isso pode resultar em um comportamento inesperado de software de escrita de mídia.

## <a name="mitigation"></a>Atenuação

Para reverter para o status always-on, desligue essa funcionalidade no Registro. O caminho absoluto para o valor do Registro é:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Seu tipo é DWORD (32 bits) e, se seu valor for 0, o ZPODD será desabilitado; se for qualquer outro valor, o ZPODD será habilitado.

## <a name="tests"></a>Testes

Teste o software de escrita de mídia em busca de anomalias que ocorram devido a esse novo recurso. Informe [a Microsoft](mailto:OptIssue@microsoft.com) sobre os problemas que encontrar com esse novo recurso.

 

 




