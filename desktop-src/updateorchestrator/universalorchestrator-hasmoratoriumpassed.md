---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Consulta o Orchestrator universal para determinar se o período pós-OOBE foi superado.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105780763"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>Método IUniversalOrchestrator:: HasMoratoriumPassed

> [!NOTE] 
> Essa API pertence à API do Orchestrator universal.

Permite que os clientes determinem se o universal Orchestrator está operando imediatamente após o novo dispositivo de experiência inicial, o que limita as tentativas de trabalho de minimizar a interrupção do usuário. 

## <a name="syntax"></a>Sintaxe

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Parâmetros

`callerIdentifier`

Uma cadeia de caracteres exclusiva que identifica todas as chamadas desse cliente específico.

`hasMoratoriumPassed`

Parâmetro de saída que armazena o resultado da consulta.

## <a name="return-value"></a>Retornar valor
Se esse método tiver sucesso, ele retornará **S_OK**.  Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |



 

 



