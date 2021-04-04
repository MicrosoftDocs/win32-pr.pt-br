---
title: LocalService
description: Instala um objeto como um aplicativo de serviço.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- COM valor de registro LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824018"
---
# <a name="localservice"></a><span data-ttu-id="0b096-104">LocalService</span><span class="sxs-lookup"><span data-stu-id="0b096-104">LocalService</span></span>

<span data-ttu-id="0b096-105">Instala um objeto como um aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="0b096-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0b096-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="0b096-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="0b096-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b096-107">Remarks</span></span>

<span data-ttu-id="0b096-108">Além de serem executados como um executável de servidor local (EXE), um objeto COM também pode optar por empacotar para ser executado como um aplicativo de serviço quando ativado por um cliente local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0b096-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="0b096-109">Os serviços dão suporte a vários recursos administrativos úteis e integrados à interface do usuário, incluindo início, parada, pausa e reinicialização locais e remotos, bem como a capacidade de estabelecer o servidor para ser executado em uma conta de usuário e estação de janela específicas.</span><span class="sxs-lookup"><span data-stu-id="0b096-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="0b096-110">Um objeto escrito como um serviço é instalado para ser usado pelo COM, estabelecendo um valor de **LocalService** e executando uma instalação de serviço padrão.</span><span class="sxs-lookup"><span data-stu-id="0b096-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="0b096-111">O valor **LocalService** deve ser definido como o nome do serviço, conforme configurado em **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**, como o valor de **\_ sz padrão reg** .</span><span class="sxs-lookup"><span data-stu-id="0b096-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="0b096-112">Quando o **LocalService** é definido, qualquer cadeia de caracteres atribuída a [**serviceparameters**](serviceparameters.md) é passada como um argumento de linha de comando para o serviço à medida que ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0b096-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="0b096-113">A configuração de serviço é preferida em muitas situações em que os recursos das APIs de gerenciamento de serviço local e remoto e a interface do usuário podem ser úteis para os serviços que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="0b096-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="0b096-114">Por exemplo, aproveitar a estrutura administrativa existente da arquitetura de serviço deve ser uma opção óbvia se o objeto for de longa duração ou der suporte imediato a conceitos como iniciar, parar, redefinir ou pausar.</span><span class="sxs-lookup"><span data-stu-id="0b096-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="0b096-115">Os serviços podem ser configurados dinamicamente e podem ser configurados para serem executados automaticamente quando o computador é inicializado, ou para serem iniciados quando solicitado por um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0b096-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="0b096-116">Se você estiver implementando classes como serviços, deve estar ciente dos seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="0b096-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="0b096-117">Esse valor é usado em preferência à chave [**LocalServer32**](localserver32.md) para ativação local e remota requestsâ € "se o **LocalService** existir e se referir a um serviço válido, a chave **LocalServer32** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="0b096-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="0b096-118">Atualmente, apenas uma única instância de um aplicativo de serviço pode estar sendo executada em um determinado momento em um computador.</span><span class="sxs-lookup"><span data-stu-id="0b096-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="0b096-119">Os serviços COM devem, portanto, registrar seus objetos de classe na inicialização usando REGCLS \_ MULTIPLEUSE para dar suporte a vários clientes.</span><span class="sxs-lookup"><span data-stu-id="0b096-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="0b096-120">Para iniciar e inicializar corretamente, os serviços COM configurados para serem executados automaticamente quando um computador é inicializado devem incluir RPCSs na lista de serviços dependentes.</span><span class="sxs-lookup"><span data-stu-id="0b096-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b096-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b096-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b096-122">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="0b096-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="0b096-123">**Serviceparameters**</span><span class="sxs-lookup"><span data-stu-id="0b096-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="0b096-124">Serviços</span><span class="sxs-lookup"><span data-stu-id="0b096-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 