---
description: Com o tempo, versões diferentes de TAPI, aplicativos e provedores de serviços podem ser produzidos.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Controle de versão da TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297006"
---
# <a name="tapi-versioning"></a>Controle de versão da TAPI

Com o tempo, versões diferentes de TAPI, aplicativos e provedores de serviços podem ser produzidos. Essas novas versões podem fazer novas definições, como para novos recursos, novos membros em estruturas de dados e novos campos de bits. Portanto, os números de versão são necessários para indicar como interpretar várias estruturas de dados.

Para permitir a interoperabilidade ideal de diferentes versões de aplicativos, versões da própria TAPI e versões de provedores de serviço por diferentes fornecedores, a telefonia da Microsoft fornece um mecanismo de negociação de versão simples para aplicativos. Há duas versões diferentes que a TAPI e o provedor de serviços de telefonia precisam concordar em cada dispositivo de linha. A primeira é a versão negociada com a TAPI e o provedor de serviços de telefonia (TSP) básico e a telefonia suplementar, conhecida como a versão da interface TAPI. O outro é para extensões específicas do provedor, se houver, e é chamado de versão de extensão. O formato das estruturas de dados e dos tipos de dados usados pelos recursos básicos e complementares da TAPI é definido pela versão da TAPI, enquanto a versão da extensão determina o formato das estruturas de dados definidas pelas extensões específicas do fornecedor.

A função [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) negocia uma versão TAPI e o [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negocia a versão de extensão do tsp. Um único TSP pode ser capaz de lidar com mais de uma versão, e um aplicativo deve fazer "fallback" para usar uma versão mais antiga, se estiver usando um TSP mais antigo. Em **lineNegotiateAPIVersion** , o parâmetro *dwApiVersion* usa como padrão um valor de acordo com a versão, da seguinte maneira.



| Versão da TAPI | Valor padrão |
|--------------|---------------|
| 1,3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2,0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

No entanto, a TAPI torna isso muito mais fácil, desde que o próprio TSP esteja usando uma versão mais recente do que o aplicativo. Se o TSP for realmente mais recente, a TAPI será capaz de traduzir "para baixo" para a versão do aplicativo. Por exemplo, a TAPI 2,0 TSPs não precisa ser especificamente capaz de lidar com a TAPI versão 1,4. Se um aplicativo TAPI 1,4 for executado, a TAPI converterá todas as estruturas e mensagens da TAPI 2,0 em equivalentes a TAPI 1,4 ou o mais próximo possível. Se não houver uma aproximação próxima no TAPI 1,4, todas as informações específicas da TAPI 2,0 serão perdidas.

O significado preciso de uma versão de extensão é específico do provedor. Para usar um TSP que ofereça suporte a extensões, consulte a documentação do provedor.

Há várias versões da TAPI. Embora a maioria dessas versões envolvam alterações nos conjuntos de documentação da TAPI e da TSPI (interface do provedor de serviços de telefonia), há outras implicações para cada versão, ou seja, diferenças arquitetônicas, variações de sistema operacional, redistribuíveis e problemas de desenvolvimento do TSP.



| Versão da TAPI        | Distribuição                                                   |
|---------------------|----------------------------------------------------------------|
| 1,0 – 1,2           | Versões beta que não devem mais ser usadas.              |
| [1.4](tapi-1-4.md) | Incluído no Windows 95.                                        |
| [1.5](tapi-1-5.md) | Incluído no Windows CE 1,0.                                    |
| [2.0](tapi-2-0.md) | Incluído no Windows NT 4,0 com SP3.                           |
| [2.1](tapi-2-1.md) | Incluído no Windows NT 4,0 com SP4 e Windows 98.            |
| [2.2](tapi-2-2.md) | Incluído no Windows Server 2003, Windows XP e Windows 2000. |



 

 

 



