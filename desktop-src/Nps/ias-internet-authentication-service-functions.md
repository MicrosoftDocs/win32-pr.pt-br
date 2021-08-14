---
title: Funções de extensões NPS
description: Funções de extensões NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cecf8ead61e94287ba4846b82f922af40068a771a9bcadd8ccb51693709c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362356"
---
# <a name="nps-extensions-functions"></a>Funções de extensões NPS

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008. O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

 

## <a name="application-defined"></a>Aplicativo definido

A arquitetura para DLLs de Extensão NPS dá suporte às seguintes funções exportadas:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

As [**funções RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) [**e RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) são opcionais.

A DLL de extensão pode exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) em vez de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) ou [**RadiusExtensionProcessEx.**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)

Se a DLL de extensão exportar [**RadiusExtensionProcessEx,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)ela também deverá exportar [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Definido pelo sistema

Quando o NPS chama uma implementação [**de RadiusExtensionProcess2,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)o NPS passa a função um ponteiro para uma estrutura [**RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK.**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)

A [**estrutura RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contém ponteiros de função para as seguintes funções fornecidas pelo NPS:

-   [**Getrequest**](/previous-versions/ms688263(v=vs.85))
-   [**Getresponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

As funções [**GetRequest**](/previous-versions/ms688263(v=vs.85)) e [**GetResponse**](/previous-versions/ms688270(v=vs.85)) retornam ponteiros para uma estrutura do tipo [**RADIUS ATTRIBUTE \_ \_ ARRAY.**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)

A [**estrutura RADIUS ATTRIBUTE \_ \_ ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contém ponteiros de função para as seguintes funções fornecidas pelo NPS:

-   [**Adicionar**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**Getsize**](/previous-versions/ms688277(v=vs.85))
-   [**Insertat**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**Setat**](/previous-versions/ms688456(v=vs.85))

 

 