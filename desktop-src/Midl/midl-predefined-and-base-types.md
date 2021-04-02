---
title: Tipos de base e predefinidos MIDL
description: O MIDL dá suporte aos seguintes tipos de base e predefinidos.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- tipos de dados MIDL, predefinidos e base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1afaa479969d65f162a9d57935aa7fbc539701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005402"
---
# <a name="midl-predefined-and-base-types"></a>Tipos de base e predefinidos MIDL

O MIDL dá suporte aos seguintes tipos de base e predefinidos.



| Tipo de dados                                  | Descrição                                                                                                                                                                                             | Sinal padrão     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**Boolean**](boolean.md)                 | 8 bits. Não compatível com interfaces [**oleautomation**](oleautomation.md) ; \_em vez disso, use Variant bool.                                                                                               | Não assinado         |
| [**minuciosa**](byte.md)                       | 8 bits.                                                                                                                                                                                                 | (não se aplica) |
| [**º**](char-idl.md)                   | 8 bits.                                                                                                                                                                                                 | Não assinado         |
| [**double**](double.md)                   | número de ponto flutuante de 64 bits.                                                                                                                                                                           | (não se aplica) |
| [**status de erro \_ \_ t**](error-status-t.md) | inteiro de 32 bits sem sinal para retornar valores de status para tratamento de erro.                                                                                                                                 | Não assinado         |
| [**float**](float.md)                     | número de ponto flutuante de 32 bits.                                                                                                                                                                           | (não se aplica) |
| [**lidar com \_ t**](handle-t.md)              | Tipo de identificador primitivo para associação.                                                                                                                                                                      | (não se aplica) |
| [**Hyper**](hyper.md)                     | inteiro de 64 bits.                                                                                                                                                                                         | Com sinal           |
| [**INT**](int.md)                         | inteiro de 32 bits. Em plataformas de 16 bits, o não pode aparecer em funções remotas sem um qualificador de tamanho como [**curto**](short.md), [**pequeno**](small.md), [**longo**](long.md) ou [**Hyper**](hyper.md). | Com sinal           |
| **\_\_int8**                               | inteiro de 8 bits. Equivalente a **pequeno**.                                                                                                                                                                 | Com sinal           |
| **\_\_Int16**                              | inteiro de 16 bits. Equivalente a **Short**.                                                                                                                                                                | Com sinal           |
| **\_\_Int32**                              | inteiro de 32 bits. Equivalente a [**Long**](long.md).                                                                                                                                                     | Com sinal           |
| [**\_\_int3264**](--int3264.md)           | Um inteiro que é de 32 bits em plataformas de 32 bits e é de 64 bits em plataformas de 64 bits.                                                                                                                       | Com sinal           |
| [**\_\_Int64**](--int64.md)               | inteiro de 64 bits. Equivalente a [**Hyper**](hyper.md).                                                                                                                                                   | Com sinal           |
| [**Longas**](long.md)                       | inteiro de 32 bits.                                                                                                                                                                                         | Com sinal           |
| [**short**](short.md)                     | inteiro de 16-BT.                                                                                                                                                                                          | Com sinal           |
| [**menores**](small.md)                     | inteiro de 8 bits.                                                                                                                                                                                          | Com sinal           |
| [**void**](void.md)                       | Indica que o procedimento não retorna um valor.                                                                                                                                                   | (não se aplica) |
| **livre \***                                | ponteiro de 32 bits somente para identificadores de contexto.                                                                                                                                                                | (não se aplica) |
| [**WCHAR \_ t**](wchar-t.md)                | tipo predefinido de 16 bits para caracteres largos.                                                                                                                                                             | Não assinado         |



 

 

 




