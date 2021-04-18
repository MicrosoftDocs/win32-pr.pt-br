---
description: As provisões são feitas para estender constantes e estruturas tanto de forma independente de dispositivo quanto de um modo específico de dispositivo (específico do fornecedor).
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Extensibilidade constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a470ccb52af1bdc92596ac42bbafb74d4821db1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759973"
---
# <a name="constant-extensibility"></a>Extensibilidade constante

As provisões são feitas para estender constantes e estruturas tanto de forma independente de dispositivo quanto de um modo específico de dispositivo (específico do fornecedor).

Em constantes que são enumerações escalares, um intervalo de valores é reservado para futuras extensões comuns. O restante dos valores é identificado como dispositivo específico. Um fornecedor pode definir significados para esses valores de qualquer forma desejada. A interpretação desses valores é codificada para a ID de extensão fornecida por meio da estrutura de dados [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Para constantes definidas como sinalizadores de bit, um intervalo de bits de ordem inferior é reservado, no qual os bits de ordem superior podem ser específicos da extensão. É recomendável que os valores estendidos e matrizes de bits usem bits do valor mais alto ou de um bit de ordem superior. Isso deixa a opção de mover a borda entre a parte comum e a parte de extensão, se necessário, para fazer isso no futuro. As extensões para estruturas de dados são atribuídas a um campo tamanho em variavelmente com tamanho/deslocamento sendo parte da parte fixa. TSPI descreve quais extensões específicas de dispositivo são permitidas para cada estrutura de dados. Para obter mais informações, consulte o tópico [alocação de memória](./memory-allocation.md) .

Além de reconhecer um identificador de extensão específico, a TAPI (operando em nome de um aplicativo) deve negociar o número de versão da extensão em que o aplicativo e o provedor de serviço operarão. Isso é feito usando as funções [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) e [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Um identificador de extensão é um identificador global exclusivo. Não há registro central para identificadores de extensão. Em vez disso, eles são gerados localmente pelo fabricante por um utilitário que está disponível com o kit de ferramentas. Para garantir a exclusividade global, o número é composto de partes como um endereço de LAN (exclusivo), hora do dia e um número aleatório. Identificadores globalmente exclusivos são projetados para serem distinguíveis de identificadores universais exclusivos do HP/DEC e são, portanto, totalmente compatíveis com eles.

 

 
