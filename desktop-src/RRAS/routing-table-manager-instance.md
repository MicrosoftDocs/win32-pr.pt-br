---
title: Instância do Gerenciador de tabela de roteamento
description: Uma instância é uma tabela separada que o Gerenciador de tabela de roteamento usa para manter informações de roteamento sobre um subconjunto de interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3215baf7a3cf093ecf47e8cf9965a71e75dea17a0527949e68b2c5f929d336ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073916"
---
# <a name="routing-table-manager-instance"></a>Instância do Gerenciador de tabela de roteamento

Uma instância é uma tabela separada que o Gerenciador de tabela de roteamento usa para manter informações de roteamento sobre um subconjunto de interfaces. Normalmente, as instâncias são usadas para permitir que um roteador físico atue como um conjunto de roteadores virtuais – um roteador virtual por rede lógica.

Atualmente, o Gerenciador de tabela de roteamento dá suporte a apenas uma instância (identificada como zero, o padrão). O cliente pode se registrar em outras instâncias, mas nenhum roteador virtual, exceto o padrão, é reconhecido ou usado pelo Gerenciador de roteador.

 

 




