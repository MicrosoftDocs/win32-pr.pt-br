---
description: Os serviços de telefonia suplementares são a coleção de todos os serviços definidos pela API que não são os incluídos no subconjunto de telefonia básico.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Serviços de telefonia suplementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828325"
---
# <a name="supplementary-telephony-services"></a>Serviços de telefonia suplementares

Os serviços de telefonia suplementares são a coleção de todos os serviços definidos pela API que não são os incluídos no subconjunto de telefonia básico. Ele inclui todos os chamados recursos suplementares encontrados em PBXs modernos, como retenção, transferência, conferência, estacionamento e assim por diante. Todos os recursos complementares são considerados opcionais; ou seja, o provedor de serviços decide quais desses serviços ele faz ou não fornece.

Um aplicativo pode consultar um dispositivo de linha ou telefone para o conjunto de serviços complementares que ele fornece usando funções como [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) ou [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps). Um único serviço suplementar pode consistir em várias chamadas de função e mensagens. A API de telefonia, e não o desenvolvedor do provedor de serviços, define o comportamento de cada um desses recursos complementares. Um provedor de serviços deve fornecer um serviço de telefonia suplementar somente se ele puder implementar o significado exato conforme definido pela API. Caso contrário, o recurso deve ser fornecido como um serviço de telefonia estendido.

Conforme mencionado em serviços de telefonia básicos, os serviços de dispositivo de telefone são considerados opcionais. Portanto, todos os serviços de dispositivo telefônico fazem parte da telefonia suplementar. Para obter uma lista das funções de telefonia suplementar, consulte referência de [função rápida TAPI](./tapi-quick-function-reference.md).

 

 
