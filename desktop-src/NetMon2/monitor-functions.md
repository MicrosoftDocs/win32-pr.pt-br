---
description: Esta seção descreve as funções auxiliares que você pode usar para desenvolver monitores personalizados.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Monitorar funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a46aff05c9d8775edf5bb233cb18f288dc7ba4d65ba0300370ee7ede3a2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677096"
---
# <a name="monitor-functions"></a>Monitorar funções

Esta seção descreve as funções auxiliares que você pode usar para desenvolver monitores personalizados.



| Função                                       | Descrição                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Cria uma instância do monitor.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Converte uma cadeia de caracteres de versão HTML CP \_ UTF8 em Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Carrega um **DWORD de uma** cadeia de caracteres de configuração HTML.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Carrega uma lista de endereços IP de uma cadeia de caracteres de configuração HTML TEXTAREA.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Carrega uma lista de endereços IPX de uma cadeia de caracteres de configuração HTML TEXTAREA.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Carrega uma lista de endereços MAC de uma cadeia de caracteres de configuração HTML TEXTAREA.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Transforma uma cadeia de caracteres (como "157.54.32.45") em um **endereço DWORD.**                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Pesquisa um nome de variável solicitado na cadeia de caracteres de configuração e aloca espaço suficiente (usando **HeapAllocMemory**) para armazená-lo, copiá-lo e devolvê-lo. |
| [OnLoadingDLL](onloadingdll.md)               | Indica que a DLL começou a ser carregada. O MCSVC chama essa função quando carrega a DLL do monitor pela primeira vez.                                                     |



 

 

 



