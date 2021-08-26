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
ms.openlocfilehash: 1ebe9ab0232104886078256effdfaf5534144dc30421dab2ac2359ef390c0a69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118146"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



