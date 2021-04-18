---
description: Depois que sua extensão de snap-in de anexo tiver sido adicionada ao nó de serviços, ela deverá estabelecer a comunicação com o snap-in de configuração de segurança.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Estabelecendo a comunicação com snap-ins de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787447"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>Estabelecendo a comunicação com snap-ins de configuração

Depois que sua extensão de snap-in de anexo tiver sido adicionada ao nó de serviços, ela deverá estabelecer a comunicação com o snap-in de configuração de segurança. Isso é necessário porque a extensão do snap-in de anexos obtém seus dados, bem como quaisquer alterações feitas pelo usuário, do snap-in de configuração de segurança. Isso pode ser feito conforme descrito no procedimento a seguir.

**Para estabelecer a comunicação com os snap-ins de configuração de segurança**

1.  Obtenha o nome do arquivo de configuração usando o \_ formato de área de transferência de anexos CCF SCESVC \_ , que retorna o nome do arquivo de configuração como um **PWSTR**.

    Se o anexo for inserido em um nó de tipo de configuração, o anexo precisará saber qual configuração é. (Ele comunica essas informações aos snap-ins de configuração de segurança durante a inicialização da interface.) Nesse caso, use o código a seguir.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Configure o contexto com os snap-ins de configuração de segurança. Depois que o nome da configuração for conhecido ou se o nó do serviço for um nó de análise, a extensão do snap-in do anexo deverá chamar [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para configurar o contexto, conforme mostrado no exemplo a seguir.

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> Quando você terminar de usar o identificador retornado por [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), feche o identificador chamando a função [**ISceSvcAttachmentData:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) . Isso normalmente é feito quando o usuário fecha o console do MMC.

 

 

 



