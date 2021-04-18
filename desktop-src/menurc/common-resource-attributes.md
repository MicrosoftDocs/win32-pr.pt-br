---
title: Atributos de recursos comuns
description: As instruções de definição de recurso com suporte no Windows de 16 bits incluem uma opção Load-mem que especifica as características de carga e memória do recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813590"
---
# <a name="common-resource-attributes"></a>Atributos de recursos comuns

As instruções de definição de recurso com suporte no Windows de 16 bits incluem uma opção *Load-mem* que especifica as características de carga e memória do recurso. Esses atributos são permitidos em scripts de recurso para compatibilidade com versões anteriores, mas são ignorados. Os recursos do Windows são carregados quando o módulo correspondente é carregado e liberados quando o módulo é descarregado.

## <a name="load-attributes"></a>Carregar atributos

Os atributos de carregamento especificam quando o recurso deve ser carregado. O parâmetro de carregamento deve ser um dos atributos a seguir.



| Atributo      | Descrição                                                                  |
|----------------|------------------------------------------------------------------------------|
| **CARREGAMENTO**    | Ignorado. No Windows de 16 bits, o recurso é carregado com o arquivo executável. |
| **LOADONCALL** | Ignorado. No Windows de 16 bits, o recurso é carregado quando chamado.              |



 

## <a name="memory-attributes"></a>Atributos de memória

Os atributos de memória especificam se o recurso é fixo ou móvel, se é Descartado e se é puro. O parâmetro de memória pode ser um ou mais dos atributos a seguir.



| Atributo       | Descrição                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignorado. No Windows de 16 bits, o recurso permanece em um local de memória fixa.                                                              |
| **MÓVEL**    | Ignorado. No Windows de 16 bits, o recurso pode ser movido, se necessário, para compactar a memória.                                                     |
| **Descartado** | Ignorado. No Windows de 16 bits, o recurso poderá ser Descartado se não for mais necessário.                                                            |
| **MERO**        | Ignorado. Aceito para compatibilidade com scripts de recursos existentes.                                                                       |
| **IMPUROS**      | Ignorado. Aceito para compatibilidade com scripts de recursos existentes.                                                                       |
| **COMPARTILHADO**      | Ignorado. No Windows de 16 bits, SHARED é ignorado para módulos regulares. Para um recurso de um módulo de ROM do Windows, a memória é compartilhada.        |
| **Não compartilhado**   | Ignorado. No Windows de 16 bits, não compartilhado é ignorado para módulos regulares. Para um recurso de um módulo de ROM do Windows, a memória não é compartilhada. |



 

 

 




