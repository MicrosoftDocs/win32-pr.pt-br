---
title: Registrando um servidor EXE em execução
description: Registrando um servidor EXE em execução
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292585"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="b9926-103">Registrando um servidor EXE em execução</span><span class="sxs-lookup"><span data-stu-id="b9926-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="b9926-104">Quando um servidor executável (EXE) é iniciado, ele deve chamar [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), que registra o CLSID para o servidor no que é chamado de tabela de classe (uma tabela diferente da tabela de objetos em execução).</span><span class="sxs-lookup"><span data-stu-id="b9926-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="b9926-105">Quando um servidor é registrado na tabela de classes, ele permite que o SCM (Gerenciador de controle de serviço) determine que não é necessário iniciar a classe novamente, porque o servidor já está em execução.</span><span class="sxs-lookup"><span data-stu-id="b9926-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="b9926-106">Somente se o servidor não estiver listado na tabela de classe, o SCM verificará os valores apropriados no registro e iniciará o servidor associado ao CLSID fornecido.</span><span class="sxs-lookup"><span data-stu-id="b9926-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="b9926-107">Você passa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) o CLSID para a classe e um ponteiro para sua interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b9926-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b9926-108">Os clientes que, posteriormente, chamam o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) com esse CLSID recuperarão um ponteiro para a interface solicitada, desde que a segurança não proíba isso.</span><span class="sxs-lookup"><span data-stu-id="b9926-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="b9926-109">(Consulte [funções auxiliares de criação de instância](instance-creation-helper-functions.md) para obter uma descrição de várias funções de criação e ativação de instância.)</span><span class="sxs-lookup"><span data-stu-id="b9926-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="b9926-110">O servidor para um objeto de classe deve chamar [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) para revogar o objeto de classe (remover seu registro) quando todas as seguintes opções forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="b9926-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="b9926-111">Não há instâncias existentes da definição de objeto.</span><span class="sxs-lookup"><span data-stu-id="b9926-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="b9926-112">Não há bloqueios no objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="b9926-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="b9926-113">O aplicativo que fornece serviços para o objeto de classe não está sob controle de usuário (não visível para o usuário na exibição).</span><span class="sxs-lookup"><span data-stu-id="b9926-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9926-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9926-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9926-115">Instalando como um aplicativo de serviço</span><span class="sxs-lookup"><span data-stu-id="b9926-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="b9926-116">Registrando uma classe na instalação</span><span class="sxs-lookup"><span data-stu-id="b9926-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="b9926-117">Registrando objetos no corrompidos</span><span class="sxs-lookup"><span data-stu-id="b9926-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="b9926-118">Registro automático</span><span class="sxs-lookup"><span data-stu-id="b9926-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




