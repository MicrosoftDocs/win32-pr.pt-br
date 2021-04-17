---
title: Abrindo e fechando arquivos
description: Abrindo e fechando arquivos
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- Função AVIFileOpen
- Função AVIFileRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105761889"
---
# <a name="opening-and-closing-files"></a>Abrindo e fechando arquivos

Um aplicativo deve abrir um arquivo AVI antes de ler ou gravar. Para abrir um arquivo AVI, use a função [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) . **AVIFileOpen** retorna o endereço de uma interface de arquivo AVI que contém o identificador do arquivo aberto e incrementa a contagem de referência do arquivo.

A função **AVIFileOpen** dá suporte ao dos sinalizadores usados com a função [OpenFile](/documentation/) . Se um aplicativo gravar em um arquivo existente, ele deverá incluir o \_ sinalizador de gravação em **AVIFileOpen**. Da mesma forma, se seu aplicativo cria e grava em um novo arquivo, você deve incluir os \_ sinalizadores de criação e de \_ gravação em **AVIFileOpen**.

Quando você abre um arquivo usando **AVIFileOpen**, pode usar um manipulador de arquivo padrão ou pode especificar um manipulador de arquivo personalizado para ler e gravar no arquivo e seus fluxos de dados. Em ambos os casos, AVIFile pesquisa no registro o manipulador de arquivo correto a ser usado. Você deve garantir que os manipuladores de arquivo personalizados estejam no registro antes que um aplicativo possa acessá-los.

Você pode incrementar a contagem de referência de um arquivo usando a função [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) . Por exemplo, talvez você queira fazer isso ao passar um identificador da interface de arquivo para outro aplicativo ou quando desejar manter um arquivo aberto ao usar uma função que normalmente fecharia o arquivo.

Você pode fechar um arquivo usando a função [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) . A função **AVIFileRelease** decrementa a contagem de referência de um arquivo AVI, salva as alterações feitas no arquivo e, quando a contagem de referência chega a zero, fecha o arquivo. Seus aplicativos devem balancear a contagem de referência incluindo uma chamada para **AVIFileRelease** para cada uso de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileAddRef**.

> [!Note]  
> Um aplicativo pode abrir um arquivo com um ou mais threads de programa. No entanto, para o melhor desempenho possível, apenas um thread deve acessar o arquivo a qualquer momento.

 

 

 