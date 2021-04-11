---
title: Registrando uma classe na instalação
description: Se uma classe for destinada a estar disponível para os clientes a qualquer momento, como a maioria dos aplicativos, você normalmente o registrará por meio de um programa de instalação e instalação.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294532"
---
# <a name="registering-a-class-at-installation"></a>Registrando uma classe na instalação

Se uma classe for destinada a estar disponível para os clientes a qualquer momento, como a maioria dos aplicativos, você normalmente o registrará por meio de um programa de instalação e instalação. Isso significa colocar informações sobre o aplicativo no registro, incluindo como e onde seus objetos devem ser instanciados. Essas informações devem ser registradas para todos os CLSIDs. Outras informações são opcionais. Ferramentas como o regsvr32 simplificam a gravação de um programa de instalação que registra servidores na instalação.

Se você não depender de padrões do sistema, haverá duas chaves importantes no registro: CLSID e AppID. Entre as informações importantes sob essas chaves está como o objeto deve ser instanciado. Os objetos podem ser designados como em processo, fora do processo local ou remoto fora do processo.

Na chave AppID há vários valores que definem informações específicas para esse aplicativo. Entre eles estão [RemoteServerName](remoteservername.md) e [ActivateAtStorage](activateatstorage.md), ambos podem ser usados para permitir que um cliente crie um objeto, com o cliente sem conhecimento interno do local do servidor. (Para obter mais informações sobre a instanciação remota, consulte [localizando um objeto remoto](locating-a-remote-object.md) e [funções auxiliares de criação de instância](instance-creation-helper-functions.md).)

Um servidor também pode ser instalado como um serviço ou para ser executado em uma conta de usuário específica. Para obter mais informações, consulte [instalando como um aplicativo de serviço](installing-as-a-service-application.md).

Um servidor ou objeto corrompidos que não seja um serviço ou em execução em uma conta de usuário específica pode ser chamado de servidor "Activate as Activator". Para esses servidores, o contexto de segurança e a estação da janela/área de trabalho do cliente devem corresponder ao do servidor. Um cliente que está tentando se conectar a um servidor remoto é considerado uma estação de janela/área de trabalho **nula** , portanto, somente o contexto de segurança do servidor é comparado nessa instância. (Para obter mais informações sobre SIDs, consulte [segurança em com](security-in-com.md).) O COM armazena em cache a estação de janela/área de trabalho de um processo quando o processo se conecta pela primeira vez ao serviço COM distribuído. Portanto, os clientes e servidores COM não devem alterar sua estação de janela ou desktops de thread do processo depois de chamar o [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

Quando uma classe é registrada como em processo, uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) para criar seu objeto de classe é passada automaticamente pelo com para a função [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , que a classe deve implementar para dar ao objeto de chamada um ponteiro para seu objeto de classe.

As classes implementadas em executáveis podem especificar que o COM deve executar seu processo e aguardar que o processo Registre a interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) do seu objeto de classe por meio de uma chamada para a função [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chaves do registro COM](com-registry-keys.md)
</dt> <dt>

[Instalando como um aplicativo de serviço](installing-as-a-service-application.md)
</dt> <dt>

[Registrando um servidor EXE em execução](registering-a-running-exe-server.md)
</dt> <dt>

[Registrando componentes](registering-components.md)
</dt> <dt>

[Registrando objetos no corrompidos](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 