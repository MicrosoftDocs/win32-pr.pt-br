---
description: Esta seção descreve as funções auxiliares que você pode usar para desenvolver monitores personalizados.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funções de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827257"
---
# <a name="monitor-functions"></a>Funções de monitor

Esta seção descreve as funções auxiliares que você pode usar para desenvolver monitores personalizados.



| Função                                       | Descrição                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Cria uma instância do monitor.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Converte uma \_ cadeia de caracteres de versão HTML CP UTF8 em Unicode.                                                                                                             |
| [Loaddword](loaddword.md)                     | Carrega um **DWORD** de uma cadeia de caracteres de configuração html.                                                                                                             |
| [Loadipaddresss](loadipaddresses.md)         | Carrega uma lista de endereços IP de uma cadeia de caracteres de configuração de TEXTAREA HTML.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Carrega uma lista de endereços IPX de uma cadeia de caracteres de configuração de TEXTAREA HTML.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Carrega uma lista de endereços MAC de uma cadeia de caracteres de configuração de TEXTAREA HTML.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Transforma uma cadeia de caracteres (como "157.54.32.45") em um endereço **DWORD** .                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Procura um nome de variável solicitado na cadeia de caracteres de configuração e aloca espaço suficiente (usando **HeapAllocMemory**) para armazená-lo, copiá-lo e retorná-lo. |
| [OnLoadingDLL](onloadingdll.md)               | Indica que a DLL começou a ser carregada. O MCSVC chama essa função quando carrega pela primeira vez a DLL do monitor.                                                     |



 

 

 



