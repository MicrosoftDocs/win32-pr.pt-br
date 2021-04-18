---
description: Os tipos de qualificador fornecem mais informações sobre um qualificador, como se uma classe ou instância derivada pode substituir o valor original dos qualificadores.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Tipos de qualificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773008"
---
# <a name="qualifier-flavors"></a>Tipos de qualificadores

Os tipos de qualificador fornecem mais informações sobre um qualificador, como se uma classe ou instância derivada pode substituir o valor original do qualificador.

Os tipos de qualificador podem ser adicionados à parte superior do arquivo MOF, usando a sintaxe a seguir, fazendo com que eles sejam aplicados em toda a definição. Por exemplo:

``` syntax
Qualifier Description : ToSubClass Amended;
```

Os tipos **ToSubClass** e **emendados** se aplicam a todos os qualificadores de **Descrição** no MOF.

A tabela a seguir lista os tipos de qualificador.



| Tipo de qualificador    | Significado                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Adicionados**         | O qualificador não é necessário na definição de classe básica e pode ser movido para o aditamento a ser localizado.                                                                                                                                  |
| **DisableOverride** | O qualificador não pode ser substituído em uma instância ou classe derivada. Observe que a capacidade de substituir um qualificador propagado é o padrão.                                                                                                      |
| **EnableOverride**  | Quando propagada para uma classe ou instância derivada, o valor do qualificador pode ser substituído. A configuração de **EnableOverride** é opcional porque a capacidade de substituir o valor do qualificador é a funcionalidade padrão para qualificadores propagados. |
| **NotToInstance**   | O qualificador não é propagado para instâncias de classe.                                                                                                                                                                                             |
| **NotToSubClass**   | O qualificador não é propagado para classes derivadas.                                                                                                                                                                                             |
| **Restricted**      | O qualificador não é propagado para instâncias ou classes derivadas.                                                                                                                                                                                |
| **ToInstance**      | O qualificador é propagado para instâncias.                                                                                                                                                                                                       |
| **ToSubClass**      | O qualificador é propagado para classes derivadas. Esse tipo é apropriado apenas para qualificadores definidos para uma classe e não pode ser anexado a um qualificador que descreve uma instância de classe.                                                           |



 

 

 



