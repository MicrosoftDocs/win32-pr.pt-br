---
description: Saiba mais sobre a extensibilidade da estrutura. As provisões são feitas para estender constantes e estruturas tanto de forma independente de dispositivo quanto de uma maneira específica ao dispositivo.
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: Extensibilidade da estrutura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378defd35304f6745d42723a44e21c0aa56a34e1f6c40c2f96d5f6743d61b805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991716"
---
# <a name="structure-extensibility"></a>Extensibilidade da estrutura

As provisões são feitas para estender constantes e estruturas tanto de forma independente de dispositivo quanto de um modo específico de dispositivo (específico do fornecedor).

Em constantes que são enumerações escalares, um intervalo de valores é reservado para futuras extensões comuns. O restante dos valores é identificado como dispositivo específico. Um fornecedor pode definir significados para esses valores de qualquer forma. A interpretação desses valores é codificada para o *identificador de extensão* fornecido por meio da estrutura de dados [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Para constantes definidas como sinalizadores de bit, um intervalo de bits de ordem inferior é reservado, no qual os bits de ordem superior podem ser específicos da extensão. É recomendável que os valores estendidos e matrizes de bits usem bits do valor mais alto ou de um bit de ordem superior. Isso deixa a opção de mover a borda entre a parte comum e a parte de extensão se for necessário fazer isso no futuro. As extensões para estruturas de dados são atribuídas a um campo tamanho em variavelmente com tamanho/deslocamento sendo parte da parte fixa. TSPI descreve para cada estrutura de dados quais extensões específicas do dispositivo são permitidas.

Além de reconhecer um identificador de extensão específico, a TAPI (operando em nome de um aplicativo) deve negociar o número de versão da extensão em que o aplicativo e o provedor de serviços operam. Isso é feito usando as funções [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) e [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Um identificador de extensão é um identificador global exclusivo. Não há registro central para identificadores de extensão. Em vez disso, eles são gerados localmente pelo fabricante por um utilitário que está disponível com o kit de ferramentas. O número é composto por partes, como um endereço de LAN (exclusivo), a hora do dia e o número aleatório, para garantir a exclusividade global. Identificadores globalmente exclusivos são projetados para serem distinguíveis de identificadores universais exclusivos do HP/DEC e são, portanto, totalmente compatíveis com eles.

 

 
