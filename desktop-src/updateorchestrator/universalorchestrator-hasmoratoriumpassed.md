---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Consulta o Orchestrator universal para determinar se o período pós-OOBE foi superado.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 3ccbf673b8fe22fabe7001112e04e87bd45eeaa4
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991793"
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

## <a name="return-value"></a>Valor retornado
Se esse método tiver sucesso, ele retornará **S_OK**.  Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |



 

 



