---
title: Registrando uma classe na instalação
description: Se uma classe for destinada a estar disponível para clientes a qualquer momento, como a maioria dos aplicativos, você geralmente a registrará por meio de um programa de instalação e instalação.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017e4393a4c5422157c8f9b9e9b7f366c2fafc8cfe6af5722e451a3d1b9fa069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047854"
---
# <a name="registering-a-class-at-installation"></a>Registrando uma classe na instalação

Se uma classe for destinada a estar disponível para clientes a qualquer momento, como a maioria dos aplicativos, você geralmente a registrará por meio de um programa de instalação e instalação. Isso significa colocar informações sobre o aplicativo no Registro, incluindo como e onde seus objetos devem ser instautados. Essas informações devem ser registradas para todas as CLSIDs. Outras informações são opcionais. Ferramentas como Regsvr32 fazem com que seja simples escrever um programa de instalação que registra servidores na instalação.

Se você não estiver confiando nos padrões do sistema, haverá duas chaves importantes no Registro: CLSID e AppID. Entre as informações importantes nessas chaves está como o objeto deve ser instautado. Os objetos podem ser designados como remotos em processo, locais fora do processo ou fora do processo.

Na chave AppID, há vários valores que definem informações específicas para esse aplicativo. Entre eles estão [RemoteServerName](remoteservername.md) e [ActivateAtStorage](activateatstorage.md), que podem ser usados para permitir que um cliente crie um objeto, com o cliente sem conhecimento integrado do local do servidor. (Para obter mais informações sobre instanciação remota, consulte [Localizando um](locating-a-remote-object.md) objeto remoto e funções [auxiliares de criação de instância .)](instance-creation-helper-functions.md)

Um servidor também pode ser instalado como um serviço ou ser executado em uma conta de usuário específica. Para obter mais informações, [consulte Instalando como um aplicativo de serviço](installing-as-a-service-application.md).

Um servidor ou objeto ROT que não é um serviço ou em execução em uma conta de usuário específica pode ser chamado de servidor "ativar como ativador". Para esses servidores, o contexto de segurança e a estação/área de trabalho da janela do cliente devem corresponder ao do servidor. Um cliente que está tentando se conectar a um servidor remoto é considerado ter uma estação/área de trabalho de janela **NULL,** portanto, somente o contexto de segurança do servidor é comparado nesta instância. (Para obter mais informações sobre SIDs, consulte [Segurança em COM](security-in-com.md).) O COM armazena em cache a estação/área de trabalho da janela de um processo quando o processo se conecta pela primeira vez ao serviço COM distribuído. Portanto, os clientes e servidores COM não devem alterar suas estações de janela ou áreas de trabalho de thread do processo depois de chamar [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

Quando uma classe é registrada como em processo, uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) para criar seu objeto de classe é passada automaticamente por COM para a [**função DllGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) que a classe deve implementar para dar ao objeto de chamada um ponteiro para seu objeto de classe.

Classes implementadas em executáveis podem especificar que COM deve executar seu processo e aguardar o processo registrar a interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) do objeto de classe por meio de uma chamada para a [**função CoRegisterClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chaves do Registro COM](com-registry-keys.md)
</dt> <dt>

[Instalando como um aplicativo de serviço](installing-as-a-service-application.md)
</dt> <dt>

[Registrando um servidor EXE em execução](registering-a-running-exe-server.md)
</dt> <dt>

[Registrando componentes](registering-components.md)
</dt> <dt>

[Registrando objetos no ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Auto-registro](self-registration.md)
</dt> </dl>

 

 