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
ms.openlocfilehash: d31d6c8ef342b9e1781297d547358317a90d515002e6ef3e529b8d7a0c50aa09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024596"
---
# <a name="application-recovery-and-restart"></a>Reinicialização e recuperação de aplicativos

## <a name="purpose"></a>Finalidade

Um aplicativo pode usar o ARR (Application Recovery and Restart) para salvar dados e informações de estado antes que o aplicativo saia devido a uma exceção sem resposta ou quando o aplicativo para de responder. O aplicativo também será reiniciado, se solicitado.

Um aplicativo também poderá ser reiniciado se um instalador atualizar um componente do aplicativo ou se o computador precisar reiniciar como resultado de uma atualização. Observe que, para dar suporte à reinicialização automática do aplicativo depois que um instalador atualiza um aplicativo, o aplicativo e o instalador precisam ser autorados adequadamente. Para obter detalhes, consulte [Registrando para reinicialização do aplicativo.](registering-for-application-restart.md)

## <a name="developer-audience"></a>Público de desenvolvedores

O ARR foi projetado para desenvolvedores C e C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O ARR está disponível a partir do sistema operacional Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                   | Descrição                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Usando a recuperação e a reinicialização do aplicativo](using-application-recovery-and-restart.md)<br/>         | Guia de procedimento para registro para recuperação e reinicialização.<br/> |
| [Referência de recuperação e reinicialização de aplicativos](application-recovery-and-restart-reference.md)<br/> | Informações de referência para a API do ARR. <br/>                    |



 

 

 





