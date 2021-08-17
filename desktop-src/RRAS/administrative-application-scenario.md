---
title: Cenário de aplicativo administrativo
description: Os aplicativos administrativos chamam um subconjunto de funções MGM relacionadas à enumeração de entradas de encaminhamento de multicast (MFEs) e estatísticas de MFE.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c8574a0e6ab85fe4e826a224377fa0de5de3851b7e31264b4c68c3c2fce56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791911"
---
# <a name="administrative-application-scenario"></a>Cenário de aplicativo administrativo

Os aplicativos administrativos chamam um subconjunto de funções MGM relacionadas à enumeração de entradas de encaminhamento de multicast (MFEs) e estatísticas de MFE. Um aplicativo não precisa se registrar no Gerenciador de grupos de multicast para usar essas funções (ou seja, o aplicativo não precisa de um identificador).

## <a name="enumerating-mfes"></a>Enumerando MFEs

A tabela a seguir resume uma série de etapas em uma interações entre um aplicativo administrativo e o Gerenciador do grupo de multicast. A primeira coluna descreve as ações que o aplicativo administrativo executa e as respostas do aplicativo administrativo para o Gerenciador do grupo de multicast. A segunda coluna descreve as respostas do Gerenciador do grupo de multicast para o aplicativo administrativo. A terceira coluna apresenta informações adicionais.

Cada linha da tabela representa uma etapa.



| Ação do aplicativo administrativo                                                                                                                                                                                      | Ação do Gerenciador de grupo multicast                                                                                                                                                                                                                                                              | Observações                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenha um ou mais MFEs usando a função [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) .                                                                                                                                   | Retornar tanta MFEs quanto couber no buffer fornecido pelo cliente. Se nenhum MFEs puder ser retornado no buffer fornecido, \_ \_ o buffer de erro de retorno será insuficiente e o tamanho do buffer necessário para retornar um MFE.<br/>                                                              | Os clientes também podem recuperar estatísticas de MFE usando as funções de estatísticas correspondentes, [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) e [**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats). |
| Se \_ o buffer insuficiente de erro \_ for recebido, chame a função [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) novamente usando um buffer do tamanho indicado.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Continue chamando a função [**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) , fornecendo como um dos parâmetros a última MFE retornada pela chamada anterior à função [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) . | Retornar tanta MFEs quanto couber no buffer fornecido pelo cliente. Se nenhum MFEs puder ser retornado no buffer fornecido, \_ \_ o buffer de erro de retorno será insuficiente e o tamanho do buffer necessário para um MFE.<br/> O erro de retorno \_ não tem \_ mais nenhum \_ item quando não resta mais MFEs.<br/> |                                                                                                                                                                                                 |
| Continue a enumeração até que o erro \_ nenhum \_ \_ item seja recebido.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Use as funções [**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) e [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) para recuperar um MFE específico ou um conjunto específico de estatísticas de MFE.

 

 

 





