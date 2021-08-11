---
title: Atributos de recurso comuns
description: As instruções de definição de recurso com suporte em Windows de 16 bits incluem uma opção load-mem que especifica as características de carregamento e memória do recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7bf01f95c700f12d130490673ef4f0df61cb84ae8077ca759655a2c4a1577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235573"
---
# <a name="common-resource-attributes"></a>Atributos de recurso comuns

As instruções de definição de recurso com suporte no Windows de 16 bits incluem uma opção *load-mem* que especifica as características de carregamento e memória do recurso. Esses atributos são permitidos em scripts de recurso para compatibilidade com backward, mas são ignorados. Windows recursos são carregados quando o módulo correspondente é carregado e são liberados quando o módulo é descarregado.

## <a name="load-attributes"></a>Atributos de carregamento

Os atributos de carga especificam quando o recurso deve ser carregado. O parâmetro de carga deve ser um dos atributos a seguir.



| Atributo      | Descrição                                                                  |
|----------------|------------------------------------------------------------------------------|
| **Pré-carga**    | Ignorado. Em 16 bits Windows, o recurso é carregado com o arquivo executável. |
| **LOADONCALL** | Ignorado. Em um Windows de 16 bits, o recurso é carregado quando chamado.              |



 

## <a name="memory-attributes"></a>Atributos de memória

Os atributos de memória especificam se o recurso é fixo ou móvel, se ele é descartável e se ele é puro. O parâmetro de memória pode ser um ou mais dos atributos a seguir.



| Atributo       | Descrição                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignorado. Em um Windows de 16 bits, o recurso permanece em um local de memória fixa.                                                              |
| **Móvel**    | Ignorado. Em 16 bits Windows, o recurso pode ser movido, se necessário, para compactar a memória.                                                     |
| **Discardable** | Ignorado. Em um Windows de 16 bits, o recurso pode ser descartado se não for mais necessário.                                                            |
| **Puro**        | Ignorado. Aceito para compatibilidade com scripts de recursos existentes.                                                                       |
| **Impuro**      | Ignorado. Aceito para compatibilidade com scripts de recursos existentes.                                                                       |
| **Compartilhado**      | Ignorado. Em 16 bits Windows, SHARED é ignorado para módulos regulares. Para um recurso de um módulo Windows ROM, a memória é compartilhada.        |
| **Compartilhada**   | Ignorado. Em 16 bits Windows, NONSHARED é ignorado para módulos regulares. Para um recurso de um módulo Windows ROM, a memória não é compartilhada. |



 

 

 




