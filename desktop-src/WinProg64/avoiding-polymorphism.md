---
title: Evitando o polimorfismo
description: Os novos tipos de dados incluem dois tipos polimórficos, INT \_ PTR e Long \_ PTR.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Programação do Windows de polimorfismo de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292714"
---
# <a name="avoiding-polymorphism"></a>Evitando o polimorfismo

Os novos tipos de dados incluem dois tipos polimórficos, **int \_ PTR** e **Long \_ PTR**. No Windows de 32 bits, o **int \_ PTR** mapeia para **int** e o **\_ PTR longo** mapeia para **Long**. No Windows de 64 bits, os dois tipos são mapeados para o tipo intrínseco **\_ \_ Int64** . O compilador MIDL dá suporte a esses tipos para chamadas de procedimento remoto, mas há uma limitação inerente que você deve ter em mente ao usá-los em um ambiente distribuído. Lembre-se de comentar seu código de acordo.

Independentemente do tamanho da plataforma, o tamanho da conexão desses tipos polimórficos é sempre de 32 bits. Ao desempacotar no Windows de 64 bits, o logon da biblioteca de tempo de execução estende os valores assinados e atribui zero aos bytes de ordem superior para um valor não assinado. Ao colocar um valor de 64 bits na transmissão, o tempo de execução trunca os bytes de ordem superior. Portanto, somente os valores de 32 bits de ordem inferior são utilizáveis.

Use os tipos polimórficos somente quando necessário para portabilidade. Para novas interfaces, use os tipos inteiros intrínsecos de MIDL **\_ \_ Int32** e **\_ \_ Int64** ou use um tipo de ponteiro ou identificador de contexto, o que for mais apropriado para o tipo de dados que está sendo transferido.

O compilador de 64 bits dá suporte a um novo **\_ \_ int3264** intrínseco de polimórfico. Novamente, esse tipo foi desenvolvido para dar suporte a esforços de portabilidade, neste caso, para dar suporte aos tipos de **\_ PTR de uint** de forma transparente. (Outro intrínseco, **\_ \_ long3264**, dará suporte ao tipo de **\_ PTR de ULong** .) Não use **\_ \_ int3264** diretamente; use o tipo **de \_ PTR** , quando precisar de um tipo polimórfico para portar motivos.

 

 




