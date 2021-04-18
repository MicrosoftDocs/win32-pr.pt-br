---
description: As classes WMI C++ que fazem parte da estrutura do provedor WMI agora são consideradas no estado final.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Classes de estrutura de provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1562d00e6b3b1563ece933ba7dd9361dd8a5d94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814544"
---
# <a name="provider-framework-classes"></a>Classes de estrutura de provedor

\[As classes WMI C++ que fazem parte da estrutura do provedor WMI agora são consideradas no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

A estrutura do provedor implementa as classes a seguir.



| Classe de estrutura                                | Descrição                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contém métodos para processamento de consulta.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contém métodos para definir e recuperar propriedades e é um encapsulamento da interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) . O implementador não deve ter que acessar os métodos **IWbemClassObject** diretamente. |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Uma classe base que fornece os mecanismos de segurança de thread internos para a estrutura do provedor WMI.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Parte da estrutura do provedor de WMI. A estrutura do provedor implementa métodos dessa interface internamente para criar novas instâncias de classes para o provedor.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e métodos que controlam o carregamento e o descarregamento do provedor de estrutura.                                                                             |
| [**Provedor**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contém funções auxiliares e fornece implementações padrão dos métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Observe que muitos dos métodos de estrutura usam parâmetros [**CHString**](chstring.md) . O **CHString** dá suporte a muitos dos mesmos métodos e propriedades que o MFC (MFC), mas sem a sobrecarga do MFC. Para obter mais informações sobre **CHString**, consulte **referência de classe CHString**.

 

 
