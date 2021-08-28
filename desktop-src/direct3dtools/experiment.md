---
description: Representa informações sobre um experimento (captura).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura do experimento
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90e60f3f197db78a3ec399c2f8ffe7144901b097
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625362"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Estrutura do experimento

Representa informações sobre um experimento (captura).

## <a name="syntax"></a>Sintaxe


```C++
} Experiment;
```

## <a name="members"></a>Membros

**processId**  
A ID do processo associado.

**applicationName**  
Uma cadeia de caracteres COM que contém o nome do aplicativo no qual executar o experimento.

**commandLineArguments**  
Uma cadeia de caracteres COM que contém os argumentos de linha de comando.

**workingDirectory**  
Uma cadeia de caracteres COM que contém o caminho do diretório de trabalho.

**tempPixRunFile**  
Uma cadeia de caracteres COM que contém o caminho de arquivo temporário usado para executar o experimento.

**startOption**  
A opção start associada ao experimento.

**experimentotype**  
O tipo de experimento (captura).

**uiLocale**  
A ID da localidade usada para elementos de sobreposição da interface do usuário durante o experiement (captura). isso é passado do host (como Visual Studio Diagnóstico de Gráficos) para o mecanismo de captura.

**registryRoot**  
Uma cadeia de caracteres COM que contém a raiz do registro. isso é passado do host (como Visual Studio Diagnóstico de Gráficos) para o mecanismo de captura.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



