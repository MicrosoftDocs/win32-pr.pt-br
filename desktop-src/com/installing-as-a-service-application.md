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
# <a name="installing-as-a-service-application"></a><span data-ttu-id="25fb3-103">Instalando como um aplicativo de serviço</span><span class="sxs-lookup"><span data-stu-id="25fb3-103">Installing as a Service Application</span></span>

<span data-ttu-id="25fb3-104">Além de serem executados como um executável de servidor local (EXE), um objeto COM também pode ser empacotado para ser executado como um aplicativo de serviço quando ativado por um cliente local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="25fb3-104">In addition to running as a local server executable (EXE), a COM object may also package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="25fb3-105">Os serviços dão suporte a vários recursos administrativos integrados e interfaceâ de usuário ", incluindo início, interrupção, pausa e reinicialização locais e remotos, bem como a capacidade de estabelecer o servidor para ser executado em uma [conta de usuário](/windows/desktop/Services/service-user-accounts) e [estação de janela](/windows/desktop/winstation/window-stations)específicas.</span><span class="sxs-lookup"><span data-stu-id="25fb3-105">Services support numerous useful and user interfaceâ€“integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific [user account](/windows/desktop/Services/service-user-accounts) and [window station](/windows/desktop/winstation/window-stations).</span></span>

<span data-ttu-id="25fb3-106">Um objeto escrito como um serviço é instalado para ser usado pelo COM, estabelecendo um valor de [LocalService](localservice.md) em sua chave [AppID](appid-key.md) e executando uma instalação de serviço padrão.</span><span class="sxs-lookup"><span data-stu-id="25fb3-106">An object written as a service is installed for use by COM by establishing a [LocalService](localservice.md) value under its [AppID](appid-key.md) key and performing a standard service installation.</span></span>

<span data-ttu-id="25fb3-107">As classes também podem ser configuradas para serem executadas em uma conta de usuário específica quando ativadas por um cliente remoto sem serem gravadas como um aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="25fb3-107">Classes may also be configured to run under a specific user account when activated by a remote client without being written as a service application.</span></span> <span data-ttu-id="25fb3-108">Para fazer isso, a classe instala um nome de usuário e uma senha a ser usada quando o SCM inicia seu processo de servidor local.</span><span class="sxs-lookup"><span data-stu-id="25fb3-108">To do this, the class installs a user name and a password to be used when the SCM launches its local server process.</span></span>

<span data-ttu-id="25fb3-109">Quando uma classe é configurada dessa maneira, as chamadas para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) com esse CLSID falharão a menos que o processo tenha sido iniciado por com em nome de uma solicitação de ativação real.</span><span class="sxs-lookup"><span data-stu-id="25fb3-109">When a class is configured in this fashion, calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID will fail unless the process was launched by COM on behalf of an actual activation request.</span></span> <span data-ttu-id="25fb3-110">Em outras palavras, as classes configuradas para execução como um usuário específico não podem ser registradas em nenhuma outra identidade.</span><span class="sxs-lookup"><span data-stu-id="25fb3-110">In other words, classes configured to run as a particular user may not be registered under any other identity.</span></span>

<span data-ttu-id="25fb3-111">O nome de usuário é extraído do valor nomeado [runas](runas.md) na chave AppID da classe.</span><span class="sxs-lookup"><span data-stu-id="25fb3-111">The user name is taken from the [RunAs](runas.md) named-value under the class's APPID key.</span></span> <span data-ttu-id="25fb3-112">Se o nome de usuário for "usuário interativo", o código de classe será executado no contexto de segurança do usuário conectado no momento e será conectado à estação de janela interativa.</span><span class="sxs-lookup"><span data-stu-id="25fb3-112">If the user name is "Interactive User", the class code is run in the security context of the currently logged on user and is connected to the interactive window station.</span></span>

<span data-ttu-id="25fb3-113">Caso contrário, a senha será recuperada de uma parte oculta do registro disponível somente para os administradores do computador e para o sistema.</span><span class="sxs-lookup"><span data-stu-id="25fb3-113">Otherwise, the password is retrieved from a hidden portion of the registry available only to administrators of the machine and to the system.</span></span> <span data-ttu-id="25fb3-114">O nome de usuário e a senha são usados para criar uma sessão de logon na qual o código de classe é executado.</span><span class="sxs-lookup"><span data-stu-id="25fb3-114">The user name and password are then used to create a logon session in which the class code is run.</span></span> <span data-ttu-id="25fb3-115">Quando iniciado dessa forma, o código de classe é executado com sua própria área de trabalho e estação de janela e não compartilha identificadores de janela, área de transferência ou outros elementos de interface do usuário com o usuário interativo ou outras classes em execução em outras contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="25fb3-115">When launched in this way, the class code runs with its own desktop and window-station and does not share window handles, the clipboard, or other user interface elements with the interactive user or other classes running in other user accounts.</span></span>

<span data-ttu-id="25fb3-116">Um servidor registrado com **LocalService** ou **runas** pode registrar um objeto na tabela de objetos em execução para permitir que qualquer cliente se conecte a ele.</span><span class="sxs-lookup"><span data-stu-id="25fb3-116">A server registered either with **LocalService** or **RunAs** can register an object in the running object table to allow any client to connect to it.</span></span> <span data-ttu-id="25fb3-117">Para fazer isso, a chamada do servidor para [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) deve definir o \_ sinalizador ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="25fb3-117">To do so, the server's call to [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) must set the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="25fb3-118">Uma configuração de servidor desse bit deve ter seu nome executável na seção AppID do registro que se refere ao AppID do executável.</span><span class="sxs-lookup"><span data-stu-id="25fb3-118">A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable.</span></span> <span data-ttu-id="25fb3-119">Um servidor "ativar como ativador" (não registrado como **LocalService** ou **runas**) pode não registrar um objeto com esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="25fb3-119">An "activate as activator" server (not registered as either **LocalService** or **RunAs**) may not register an object with this flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25fb3-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25fb3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25fb3-121">Registrando uma classe na instalação</span><span class="sxs-lookup"><span data-stu-id="25fb3-121">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="25fb3-122">Registrando um servidor EXE em execução</span><span class="sxs-lookup"><span data-stu-id="25fb3-122">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="25fb3-123">Registrando objetos no corrompidos</span><span class="sxs-lookup"><span data-stu-id="25fb3-123">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="25fb3-124">Registro automático</span><span class="sxs-lookup"><span data-stu-id="25fb3-124">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 