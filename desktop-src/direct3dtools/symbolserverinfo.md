---
description: Representa informações sobre o servidor de símbolo de depuração.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura SymbolServerInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087484"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Estrutura SymbolServerInfo

Representa informações sobre o servidor de símbolo de depuração.

## <a name="syntax"></a>Sintaxe


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Membros

**symbolPath**  
Uma cadeia de caracteres COM que contém o caminho do servidor de símbolos.

**symbolCacheDir**  
Uma cadeia de caracteres COM que contém o diretório de cache do servidor de símbolos.

**publicSymbolServerName**  
Uma cadeia de caracteres COM que contém o nome público do servidor de símbolos.

**symbolExcludeList**  
Uma cadeia de caracteres COM que especifica a lista de símbolos a serem excluídos.

**symbolIncludeList**  
Uma cadeia de caracteres COM que especifica a lista de símbolos a serem incluídos.

**useExcludeList**  
true se a lista de exclusões for ignorada; caso contrário, false.

**useMSSymbolServer**  
true se estiver usando o Microsoft Symbol Server; caso contrário, false.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



