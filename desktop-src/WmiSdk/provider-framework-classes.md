---
description: Saiba mais sobre as classes WMI C++ que fazem parte do WMI Provider Framework e agora são consideradas no estado final.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Provider Framework Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120441"
---
# <a name="provider-framework-classes"></a>Provider Framework Classes

\[As classes WMI C++ que fazem parte do WMI Provider Framework agora são consideradas no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

A estrutura do provedor implementa as classes a seguir.



| Classe Framework                                | Descrição                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contém métodos para processamento de consulta.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contém métodos para definir e recuperar propriedades e é um encapsulamento da interface [**IWbemClassObject.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) O implementador não deve ter que acessar os **métodos IWbemClassObject** diretamente. |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Uma classe base que fornece os mecanismos internos de segurança de thread para o WMI Provider Framework.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Parte do WMI Provider Framework. O Provider Framework implementa métodos dessa interface internamente para criar novas instâncias de classes para o provedor.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e métodos que controlam o carregamento e o descarregamento do provedor de estrutura.                                                                             |
| [**Provedor**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contém funções auxiliares e fornece implementações padrão dos métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Observe que muitos dos métodos de estrutura usam [**parâmetros CHString.**](chstring.md) **CHString dá** suporte a muitos dos mesmos métodos e propriedades que o MFC (MFC), mas sem a sobrecarga do MFC. Para obter mais informações sobre **CHString,** consulte **Referência de classe CHString**.

 

 
