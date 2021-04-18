---
description: Lista as interfaces fornecidas pelo mecanismo de anexo.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779345"
---
# <a name="security-management-interfaces"></a>Interfaces de gerenciamento de segurança

Esta seção contém páginas de referência para os seguintes grupos de interfaces:

-   [Interfaces do mecanismo de anexo](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Interfaces do mecanismo de anexo



| Interface                                                            | Descrição                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Recupera dados de configuração e análise sobre um serviço de segurança especificado dos snap-ins de configuração de segurança. Os snap-ins de configuração de segurança expõem essa interface, que são chamadas de extensões de snap-in de conexão para informações de análise ou configuração de consulta.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Recupera informações modificadas de configuração ou análise de um snap-in de anexo. Os snap-ins de configuração de segurança chamam essa interface para recuperar qualquer informação modificada da extensão de snap-in de anexo. O snap-in de configuração de segurança, em seguida, armazena esses dados adequadamente no banco de dado de segurança. |



 

Para obter mais informações sobre as interfaces COM que devem ser implementadas por extensões de snap-in, consulte a documentação do [console de gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

 

 
