---
title: Type-Conversion e empacotamento de atributos ACF
description: Use esses atributos para controlar como os dados são transmitidos pela rede.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- MIDL de ACF, atributos, conversão de tipos e marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286de08a56aba5ffc7b73fc52791238a6af62b3f0545e95aedabcf79d5623464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382712"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion e empacotamento de atributos ACF

Use esses atributos para controlar como os dados são transmitidos pela rede.



| Atributo                                        | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [](encode.md)[ codificação de codificação](decode.md) | Instrui o MIDL a expor as rotinas de serialização de tipo ou de procedimento (escolha) que gera para os stubs. Seu aplicativo cliente pode chamar essas rotinas para realizar marshaling de dados por valor.                                                                                                                                                                                                                                                                                  |
| [**representar \_ como**](represent-as.md)            | Especifica como um tipo de dados será representado na conexão, quando a natureza exata do tipo de dados de um cliente não for importante para o servidor (porque ele só precisa dos dados em si e não da estrutura real) ou o tipo de cliente real é desconhecido para MIDL no tempo de compilação. Por exemplo, se o aplicativo cliente usar uma lista vinculada de números de ponto flutuante, você poderá especificar que a representação de transmissão dessa lista seja uma matriz do tipo [**float**](float.md). |
| [**Marshal do usuário \_**](user-marshal.md)            | Controla como os dados são transmitidos pela rede implementando suas próprias rotinas de marshaling. Esse atributo será útil se você tiver um tipo de dados desconhecido para MIDL ou se estiver passando informações entre plataformas big endian e little-endian.                                                                                                                                                                                                                 |



 

Os atributos de marshaling de DCE [**em \_ linha**](in-line.md) e [**fora \_ de \_ linha**](out-of-line.md) não são implementados no Microsoft RPC. O compilador MIDL realiza marshaling automaticamente de tipos de dados complexos fora de linha.

 

 




