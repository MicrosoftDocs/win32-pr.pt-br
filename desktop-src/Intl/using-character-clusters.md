---
description: Os clusters de caracteres são sequências de glifos que não podem ser divididas entre as linhas.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Usando clusters de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7a48dc8ec1b6fa3ea28cd116f275b1f410b8abd7e232442cff430ab843765f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631816"
---
# <a name="using-character-clusters"></a>Usando clusters de caracteres

Os clusters de caracteres são sequências de glifos que não podem ser divididas entre as linhas. Alguns idiomas, por exemplo, tailandês e Índico, restringem o posicionamento do cursor para pontos entre clusters. Essa restrição se aplica ao movimento de cursor iniciado com ações de teclado ou mouse (teste de clique).

O Uniscribe fornece informações de cluster em ambos os atributos visuais contidos em uma estrutura [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) e os atributos lógicos contidos em uma estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Depois que o aplicativo chama [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), as informações do cluster são representadas por sequências do mesmo valor na matriz **\_ LOGATTR de script** e pelo membro **fClusterStart** no **script \_ VISATTR** array.

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) também recupera o membro **fCharStop** da estrutura [**\_ LOGATTR do script**](/windows/win32/api/usp10/ns-usp10-script_logattr) para identificar as posições do cluster.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



