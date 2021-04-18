---
description: Uma extensão de snap-in de anexo é o componente de um anexo que exibe a interface do usuário específica do serviço.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Extensões de snap-in de anexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105770323"
---
# <a name="attachment-snap-in-extensions"></a>Extensões de snap-in de anexos

Uma extensão de snap-in de anexo é o componente de um anexo que exibe a interface do usuário específica do serviço. A extensão do snap-in é hospedada pelos snap-ins de configuração de segurança. A comunicação entre a extensão de anexo e seu host de snap-in é tratada pelos mecanismos padrão do MMC descritos na documentação do [console de gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Além das interfaces para as quais a extensão de snap-in deve dar suporte para ser uma extensão de snap-in do MMC, uma extensão de snap-in de anexos também deve oferecer suporte à interface COM, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Essa interface implementa métodos que indicam se há dados específicos do serviço que devem ser salvos no banco de dado de segurança e, nesse caso, recuperar e salvar esses novos dados. Os snap-ins de configuração de segurança chamam métodos dessa interface regularmente para atualizar o banco de dados de segurança.

Os snap-ins de configuração de segurança implementam uma interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que fornece métodos para recuperar dados específicos do serviço do banco de dado de segurança. As extensões de snap-in de anexos podem chamar métodos dessa interface para recuperar dados do banco de dado de segurança.

Essa arquitetura é ilustrada no diagrama a seguir.

![extensões de snap-in de anexos](images/model2.png)

Ao criar uma extensão de snap-in de anexo, você deve instalá-la e registrá-la com os snap-ins de configuração de segurança. Você faz isso adicionando chaves ao registro, conforme explicado em [registrando uma extensão de snap-in de anexo](registering-an-attachment-snap-in-extension.md). Quando um snap-in de configuração de segurança é iniciado, ele verifica o registro e carrega todas as extensões de snap-in registradas. As extensões aparecem como nós na área de segurança para cada serviço no snap-in de configuração de segurança.

> [!Note]
> Uma extensão de snap-in de anexos só pode estender nós de serviços. O nó serviços é o snap-in do MMC que contém ferramentas para administrar serviços instalados no sistema. A extensão de snap-in de anexos declara-se como sendo subordinada a um tipo de nó de serviços específico e, em seguida, para cada ocorrência desse tipo de nó de serviços, o console do MMC adiciona automaticamente as extensões de snap-in relacionadas.
> 
> Cada extensão de snap-in de anexo possui um nó de painel de escopo e o painel de resultados relacionado no MMC.

 

 

 
