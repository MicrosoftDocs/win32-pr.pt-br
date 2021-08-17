---
description: Saiba mais sobre extensibilidade. Provisionamentos são feitos para estender constantes e estruturas de maneira independente do dispositivo e de uma maneira específica do dispositivo.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Extensibilidade (API de Telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b9b130c27ffb01131181ad0b765d6a41b3eae0bbfc84cc2ab325c3a13230a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140669"
---
# <a name="extensibility"></a>Extensibilidade

Provisionamentos são feitos para estender constantes e estruturas de maneira independente do dispositivo e de uma maneira específica do dispositivo (específica do fornecedor). Em constantes que são enumerações escalares, um intervalo de valores é reservado para extensões comuns futuras. O restante dos valores é identificado como específico do dispositivo. Um fornecedor pode definir significados para esses valores de qualquer maneira desejada. Sua interpretação é chaveada para o *identificador de extensão* fornecido na estrutura de dados [**LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) Para constantes definidas como sinalizadores de bits, um intervalo de bits de ordem baixa é reservado, em que os bits de ordem alta podem ser específicos da extensão. É recomendável que valores estendidos e matrizes de bits usem bits do valor mais alto ou bit de ordem alta para baixo. Isso deixa a opção de mover a borda entre a parte comum e a parte da extensão se houver a necessidade de fazer isso no futuro. As extensões para estruturas de dados são atribuídas a um campo de tamanho variavel com tamanho/deslocamento que faz parte da parte fixa. A TAPI descreve para cada estrutura de dados quais extensões específicas do dispositivo são permitidas.

Além de reconhecer um identificador de extensão específico, o aplicativo deve negociar o número de versão da extensão em que o aplicativo e o provedor de serviços operam. Isso é feito na segunda fase de negociação de versão da [**função lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Um identificador de extensão é um identificador global exclusivo. Não há registro central para identificadores de extensão. Em vez disso, eles são gerados localmente pelo fabricante por um utilitário que está disponível com o kit de ferramentas. O número é feito de partes como um endereço LAN exclusivo, hora do dia e número aleatório, para garantir a exclusividade global. Identificadores globalmente exclusivos são projetados para serem distinguíveis de identificadores universalmente exclusivos de HP/DEC e, portanto, são totalmente compatíveis com eles.

 

 
