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
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645885"
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
A ID da localidade usada para elementos de sobreposição da interface do usuário durante o experiement (captura). Isso é passado do host (como o Visual Studio Diagnóstico de Gráficos) para o mecanismo de captura.

**registryRoot**  
Uma cadeia de caracteres COM que contém a raiz do registro. Isso é passado do host (como o Visual Studio Diagnóstico de Gráficos) para o mecanismo de captura.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



