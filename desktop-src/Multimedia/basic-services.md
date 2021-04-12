---
title: Serviços básicos
description: Serviços básicos
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- e/s de arquivo multimídia, serviços básicos
- e/s de arquivo, serviços básicos
- entrada e saída (e/s), serviços básicos
- E/s (entrada e saída), serviços básicos
- e/s básica
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365975"
---
# <a name="basic-services"></a>Serviços básicos

O uso dos serviços de e/s básicos é semelhante ao uso dos serviços de e/s de arquivo de tempo de execução da biblioteca de tempo de execução do C. Os arquivos devem ser abertos antes que possam ser lidos ou gravados. Após a leitura ou gravação, o arquivo deve ser fechado. Você também pode alterar o local de leitura ou gravação atual em um arquivo aberto.

Antes de começar qualquer operação de e/s em um arquivo, você deve abrir o arquivo usando a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Essa função retorna um identificador de arquivo do tipo **HMMIO**. Você pode usar esse identificador de arquivo para identificar o arquivo aberto ao chamar outras funções de e/s de arquivo.

> [!Note]  
> Um identificador de arquivo **HMMIO** não é um identificador de arquivo padrão. Não use identificadores de arquivo **HMMIO** com funções de e/s de arquivo de tempo de execução do Win32 ou C.

 

Ao usar o [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para abrir um arquivo, você usa um sinalizador para especificar se você o está abrindo para leitura, gravação ou ambos. Você também pode especificar sinalizadores que permitem criar ou excluir um arquivo. Use a função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para fechar um arquivo quando terminar de ler ou gravar nele.

Você pode ler e gravar arquivos usando as funções [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) e [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , respectivamente. A próxima operação de leitura ou gravação ocorre na posição atual do arquivo ou no ponteiro do arquivo em um arquivo. A posição atual do arquivo é avançada cada vez que um arquivo é lido ou gravado.

Você também pode alterar a posição atual do arquivo usando a função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) . Você deve garantir que especifique um local válido em um arquivo. Se você especificar um local inválido, como após o final do arquivo, **mmioSeek** poderá não retornar um erro, mas as operações de e/s subsequentes poderão falhar.

Há sinalizadores que você pode usar com a função **mmioOpen** para operações além da e/s de arquivo básico. Ao especificar uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , por exemplo, você pode abrir arquivos de memória, especificar um procedimento de e/s personalizado ou fornecer um buffer para e/s armazenada em buffer.

 

 