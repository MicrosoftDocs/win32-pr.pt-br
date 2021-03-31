---
title: Reinicialização e recuperação de aplicativos
description: Escreva instaladores personalizados para reiniciar automaticamente um aplicativo que foi desligado para concluir uma atualização. Salve os dados e configure a recuperação do aplicativo antes de sair dos programas.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recuperação
- confiabilidade
- confiabilidade do software
- recuperação de aplicativo
- reinicialização do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822961"
---
# <a name="application-recovery-and-restart"></a>Reinicialização e recuperação de aplicativos

## <a name="purpose"></a>Finalidade

Um aplicativo pode usar a recuperação e reinicialização do aplicativo (ARR) para salvar dados e informações de estado antes que o aplicativo seja encerrado devido a uma exceção sem tratamento ou quando o aplicativo para de responder. O aplicativo também será reiniciado, se solicitado.

Um aplicativo também pode ser reiniciado se um instalador atualizar um componente do aplicativo ou se o computador precisar ser reiniciado como resultado de uma atualização. Observe que para dar suporte à reinicialização automática do aplicativo depois que um instalador atualiza um aplicativo, o aplicativo e o instalador precisam ser criados adequadamente. Para obter detalhes, consulte [registrando para reinicialização do aplicativo](registering-for-application-restart.md).

## <a name="developer-audience"></a>Público de desenvolvedores

O ARR foi projetado para desenvolvedores de C e C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O ARR está disponível a partir do sistema operacional Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                   | Descrição                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Usando a recuperação e reinicialização do aplicativo](using-application-recovery-and-restart.md)<br/>         | Guia de procedimentos para o registro para recuperação e reinicialização.<br/> |
| [Recuperação de aplicativo e referência de reinicialização](application-recovery-and-restart-reference.md)<br/> | Informações de referência para a API ARR. <br/>                    |



 

 

 





