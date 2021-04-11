---
title: Instalando como um aplicativo de serviço
description: Instalando como um aplicativo de serviço
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008412"
---
# <a name="installing-as-a-service-application"></a>Instalando como um aplicativo de serviço

Além de serem executados como um executável de servidor local (EXE), um objeto COM também pode ser empacotado para ser executado como um aplicativo de serviço quando ativado por um cliente local ou remoto. Os serviços dão suporte a vários recursos administrativos integrados e interfaceâ de usuário ", incluindo início, interrupção, pausa e reinicialização locais e remotos, bem como a capacidade de estabelecer o servidor para ser executado em uma [conta de usuário](/windows/desktop/Services/service-user-accounts) e [estação de janela](/windows/desktop/winstation/window-stations)específicas.

Um objeto escrito como um serviço é instalado para ser usado pelo COM, estabelecendo um valor de [LocalService](localservice.md) em sua chave [AppID](appid-key.md) e executando uma instalação de serviço padrão.

As classes também podem ser configuradas para serem executadas em uma conta de usuário específica quando ativadas por um cliente remoto sem serem gravadas como um aplicativo de serviço. Para fazer isso, a classe instala um nome de usuário e uma senha a ser usada quando o SCM inicia seu processo de servidor local.

Quando uma classe é configurada dessa maneira, as chamadas para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) com esse CLSID falharão a menos que o processo tenha sido iniciado por com em nome de uma solicitação de ativação real. Em outras palavras, as classes configuradas para execução como um usuário específico não podem ser registradas em nenhuma outra identidade.

O nome de usuário é extraído do valor nomeado [runas](runas.md) na chave AppID da classe. Se o nome de usuário for "usuário interativo", o código de classe será executado no contexto de segurança do usuário conectado no momento e será conectado à estação de janela interativa.

Caso contrário, a senha será recuperada de uma parte oculta do registro disponível somente para os administradores do computador e para o sistema. O nome de usuário e a senha são usados para criar uma sessão de logon na qual o código de classe é executado. Quando iniciado dessa forma, o código de classe é executado com sua própria área de trabalho e estação de janela e não compartilha identificadores de janela, área de transferência ou outros elementos de interface do usuário com o usuário interativo ou outras classes em execução em outras contas de usuário.

Um servidor registrado com **LocalService** ou **runas** pode registrar um objeto na tabela de objetos em execução para permitir que qualquer cliente se conecte a ele. Para fazer isso, a chamada do servidor para [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) deve definir o \_ sinalizador ROTFLAGS ALLOWANYCLIENT. Uma configuração de servidor desse bit deve ter seu nome executável na seção AppID do registro que se refere ao AppID do executável. Um servidor "ativar como ativador" (não registrado como **LocalService** ou **runas**) pode não registrar um objeto com esse sinalizador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando uma classe na instalação](registering-a-class-at-installation.md)
</dt> <dt>

[Registrando um servidor EXE em execução](registering-a-running-exe-server.md)
</dt> <dt>

[Registrando objetos no corrompidos](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 