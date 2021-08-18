---
description: Lista as interfaces fornecidas pelo mecanismo de anexo.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6adc6cbaa24be46508e2a4f72181c96d4ccb65e589fdad95808c65a57262b73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894323"
---
# <a name="security-management-interfaces"></a>Interfaces de gerenciamento de segurança

Esta seção contém páginas de referência para os seguintes grupos de interfaces:

-   [Interfaces do Mecanismo de Anexo](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Interfaces do Mecanismo de Anexo



| Interface                                                            | Descrição                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Recupera dados de configuração e análise sobre um serviço de segurança especificado dos snap-ins de Configuração de Segurança. Os snap-ins de Configuração de Segurança expõem essa interface, que as extensões de snap-in de anexo chamam para informações de configuração ou análise de consulta.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Recupera informações de configuração ou análise modificadas de um snap-in de anexo. Os snap-ins de Configuração de Segurança chamam essa interface para recuperar todas as informações modificadas da extensão de snap-in de anexo. O snap-in Configuração de Segurança armazena esses dados adequadamente no banco de dados de segurança. |



 

Para obter mais informações sobre as interfaces COM que devem ser implementadas por extensões de snap-in, consulte a [documentação Console de Gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) aplicativo.

 

 
