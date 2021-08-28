---
description: Representa informações sobre o servidor de símbolos de depuração.
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
ms.openlocfilehash: 28f85445e6affc006c5c0898df1c85d71693a66d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632084"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Estrutura SymbolServerInfo

Representa informações sobre o servidor de símbolos de depuração.

## <a name="syntax"></a>Sintaxe


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Membros

**Symbolpath**  
Uma cadeia de caracteres COM que contém o caminho do servidor de símbolos.

**symbolCacheDir**  
Uma cadeia de caracteres COM que contém o diretório de cache do servidor de símbolos.

**publicSymbolServerName**  
Uma cadeia de caracteres COM que contém o nome público do servidor de símbolos.

**symbolExcludeList**  
Uma cadeia de caracteres COM que especifica a lista de símbolos a excluir.

**symbolIncludeList**  
Uma cadeia de caracteres COM que especifica a lista de símbolos a incluir.

**useExcludeList**  
true se a lista de exclusão for ignorada; caso contrário, false.

**useMSSymbolServer**  
true se estiver usando o servidor de símbolos da Microsoft; caso contrário, false.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



