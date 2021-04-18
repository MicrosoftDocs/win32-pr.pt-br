---
description: Dois tipos de terminais de faixa são definidos para gravar o terminal de faixa de reprodução e a faixa de execução que, respectivamente, pertencem a e são gerenciados pelo terminal de gravação de arquivos e terminais de reprodução de arquivo.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Acompanhar terminais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789446"
---
# <a name="track-terminals"></a>Acompanhar terminais

Dois tipos de terminais de faixa são definidos: gravação de terminal de faixa de terminais e reprodução de faixa, que, respectivamente, pertence a e é gerenciado por registro de arquivo terminal e terminal de reprodução de arquivos.

Todos os terminais de faixa expõem as interfaces [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) e [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . A interface **ITTerminal** permite a seleção de terminais de faixa em fluxos ou chamadas.

> [!Note]  
> Os terminais de faixa também expõem uma interface privada, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), que o MSP usa. Os aplicativos não devem tentar acessar essa interface.

 

 

 
