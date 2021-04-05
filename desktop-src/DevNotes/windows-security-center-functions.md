---
description: As funções a seguir são usadas com a central de segurança do Windows.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Funções da central de segurança do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826112"
---
# <a name="windows-security-center-functions"></a>Funções da central de segurança do Windows

As funções a seguir são usadas com a central de segurança do Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                           | Descrição                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WscGetSecurityProviderHealth**](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | Obtém o estado de integridade agregado das categorias de provedor de segurança representadas pelos valores de enumeração do [**\_ \_ provedor de segurança WSC**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) especificado.<br/> |
| [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | Registra uma função de retorno de chamada a ser executada quando a WSC (central de segurança do Windows) detecta uma alteração que pode afetar a integridade de um dos provedores de segurança.<br/>                    |
| [**WscUnRegisterChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | Cancela um registro de retorno de chamada que foi feito por uma ligação para a função [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) .<br/>                                               |



 

 

 




