---
description: As provisões são feitas para estender constantes e estruturas tanto de forma independente de dispositivo quanto de um modo específico de dispositivo (específico do fornecedor).
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Extensibilidade (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca446a03a9bdbe6d906e7accf261645401cd937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169481"
---
# <a name="extensibility"></a>Extensibilidade

As provisões são feitas para estender constantes e estruturas tanto de forma independente de dispositivo quanto de um modo específico de dispositivo (específico do fornecedor). Em constantes que são enumerações escalares, um intervalo de valores é reservado para futuras extensões comuns. O restante dos valores são identificados como dispositivos específicos. Um fornecedor pode definir significados para esses valores de qualquer forma desejada. Sua interpretação é codificada para o *identificador de extensão* fornecido na estrutura de dados [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Para constantes definidas como sinalizadores de bit, um intervalo de bits de ordem inferior é reservado, no qual os bits de ordem superior podem ser específicos da extensão. É recomendável que os valores estendidos e matrizes de bits usem bits do valor mais alto ou de um bit de ordem superior. Isso deixa a opção de mover a borda entre a parte comum e a parte da extensão se houver a necessidade de fazer isso no futuro. As extensões para estruturas de dados são atribuídas a um campo tamanho em variavelmente com tamanho/deslocamento sendo parte da parte fixa. A TAPI descreve para cada estrutura de dados quais extensões específicas ao dispositivo são permitidas.

Além de reconhecer um identificador de extensão específico, o aplicativo deve negociar o número de versão da extensão em que o aplicativo e o provedor de serviços operam. Isso é feito na segunda fase de negociação de versão da função [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) .

Um identificador de extensão é um identificador global exclusivo. Não há registro central para identificadores de extensão. Em vez disso, eles são gerados localmente pelo fabricante por um utilitário que está disponível com o kit de ferramentas. O número é composto por partes, como um endereço de LAN exclusivo, a hora do dia e o número aleatório, para garantir a exclusividade global. Identificadores globalmente exclusivos são projetados para serem distinguíveis de identificadores universais exclusivos do HP/DEC e são, portanto, totalmente compatíveis com eles.

 

 
