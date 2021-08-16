---
description: Os serviços de Telefonia Suplementar são a coleção de todos os serviços definidos pela API que não os incluídos no subconjunto de Telefonia Básica.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Serviços de Telefonia Suplementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9762b2d9ca74d0212170e1e87662242d3983663db024ce52018d108cc37fb883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760748"
---
# <a name="supplementary-telephony-services"></a>Serviços de Telefonia Suplementar

Os serviços de Telefonia Suplementar são a coleção de todos os serviços definidos pela API que não os incluídos no subconjunto de Telefonia Básica. Ele inclui todos os recursos suplementares chamados encontrados em PBXs modernos, como espera, transferência, conferência, parque e assim por diante. Todos os recursos suplementares são considerados opcionais; ou seja, o provedor de serviços decide qual desses serviços ele fornece ou não.

Um aplicativo pode consultar um dispositivo de linha ou telefone para o conjunto de serviços suplementares que ele fornece usando funções como [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) ou [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps). Um único serviço suplementar pode consistir em várias chamadas de função e mensagens. A API de Telefonia, e não o desenvolvedor do provedor de serviços, define o comportamento de cada um desses recursos complementares. Um provedor de serviços deve fornecer um serviço de Telefonia Suplementar somente se puder implementar o significado exato, conforme definido pela API. Caso não seja, o recurso deve ser fornecido como um serviço de Telefonia Estendida.

Conforme mencionado nos serviços básicos de Telefonia, os serviços de dispositivo de telefone são considerados opcionais. Portanto, todos os serviços de dispositivo de telefone fazem parte da Telefonia Suplementar. Para ver uma lista das funções de Telefonia Suplementar, consulte [Referência de função rápida tapi](./tapi-quick-function-reference.md).

 

 
