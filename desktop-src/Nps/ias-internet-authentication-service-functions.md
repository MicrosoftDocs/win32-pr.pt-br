---
title: Funções de extensões do NPS
description: Funções de extensões do NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813130"
---
# <a name="nps-extensions-functions"></a>Funções de extensões do NPS

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

## <a name="application-defined"></a>Definido pelo aplicativo

A arquitetura para DLLs de extensão do NPS dá suporte às seguintes funções exportadas:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

As funções [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) e [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) são opcionais.

A DLL de extensão pode exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) em vez de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) ou [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).

Se a DLL de extensão exportar [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), ela também deverá exportar [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Definido pelo sistema

Quando o NPS chama uma implementação de [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), o NPS passa a função um ponteiro para uma estrutura de bloco de [**controle de \_ extensão \_ \_ RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .

A estrutura do [**\_ bloco de \_ controle \_ de extensão RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contém ponteiros de função para as seguintes funções fornecidas pelo NPS:

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**Setresponsetype**](/previous-versions/ms688462(v=vs.85))

As funções [**GetRequest**](/previous-versions/ms688263(v=vs.85)) e [**GetResponse**](/previous-versions/ms688270(v=vs.85)) retornam ponteiros para uma estrutura do tipo [**\_ \_ matriz de atributo RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

A estrutura de [**\_ \_ matriz de atributo RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contém ponteiros de função para as seguintes funções fornecidas pelo NPS:

-   [**Adicionar**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 