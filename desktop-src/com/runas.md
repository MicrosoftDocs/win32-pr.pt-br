---
title: RunAs
description: Configura uma classe para ser executada em uma conta de usuário específica quando ativada por um cliente remoto sem ser escrita como um aplicativo de serviço.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valor do registro RunAs COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105812151"
---
# <a name="runas"></a><span data-ttu-id="09a41-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="09a41-104">RunAs</span></span>

<span data-ttu-id="09a41-105">Configura uma classe para ser executada em uma conta de usuário específica quando ativada por um cliente remoto sem ser escrita como um aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="09a41-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="09a41-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="09a41-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="09a41-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="09a41-107">Remarks</span></span>

<span data-ttu-id="09a41-108">O valor especifica o nome de usuário e deve ser um dos formulários *username*, *Domain ***\\*** username* ou da cadeia de caracteres "Interactive User".</span><span class="sxs-lookup"><span data-stu-id="09a41-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="09a41-109">Você também pode especificar as cadeias de caracteres "NT Authority \\ LocalService" (para o serviço local) e "NT Authority \\ NetworkService" (para serviço de rede).</span><span class="sxs-lookup"><span data-stu-id="09a41-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="09a41-110">Você também pode especificar a cadeia de caracteres "NT Authority \\ System" quando {*AppID \_ GUID*} se refere a um servidor com que já foi iniciado ou que tem uma entrada na tabela de classes.</span><span class="sxs-lookup"><span data-stu-id="09a41-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="09a41-111">No entanto, não é possível usar "NT Authority \\ System" com um servidor com que ainda não tenha sido iniciado.</span><span class="sxs-lookup"><span data-stu-id="09a41-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="09a41-112">A senha padrão para "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System" é "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="09a41-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="09a41-113">A partir do Windows Vista, uma senha vazia não é mais necessária para configurar as configurações de runas "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System". </span><span class="sxs-lookup"><span data-stu-id="09a41-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="09a41-114">As classes configuradas para execução como um usuário específico não podem ser registradas em nenhuma outra identidade, portanto, as chamadas para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) com esse CLSID falham, a menos que o processo tenha sido iniciado pelo com em nome de uma solicitação de ativação real.</span><span class="sxs-lookup"><span data-stu-id="09a41-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="09a41-115">O nome de usuário é obtido do valor **runas** na chave **AppID** da classe.</span><span class="sxs-lookup"><span data-stu-id="09a41-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="09a41-116">Se o nome de usuário for "usuário interativo", o servidor será executado na identidade do usuário conectado no momento e conectado à área de trabalho interativa.</span><span class="sxs-lookup"><span data-stu-id="09a41-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="09a41-117">Caso contrário, a senha será recuperada de uma parte do registro que está disponível somente para os administradores do computador e para o sistema.</span><span class="sxs-lookup"><span data-stu-id="09a41-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="09a41-118">O nome de usuário e a senha são usados para criar uma sessão de logon na qual o servidor é executado.</span><span class="sxs-lookup"><span data-stu-id="09a41-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="09a41-119">Quando iniciada dessa forma, o usuário é executado com sua própria área de trabalho e estação de janela e não compartilha identificadores de janela, área de transferência ou outros elementos de interface do usuário com usuários interativos ou outros usuários em execução em outras contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="09a41-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="09a41-120">Para estabelecer uma senha para uma classe **runas** , você deve usar a ferramenta administrativa DCOMCNFG instalada no diretório do sistema.</span><span class="sxs-lookup"><span data-stu-id="09a41-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="09a41-121">Para identidades **runas** usadas pelos servidores DCOM, a conta de usuário especificada no valor deve ter os direitos de fazer logon como um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="09a41-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="09a41-122">Esse direito pode ser adicionado usando a ferramenta administrativa política de segurança local.</span><span class="sxs-lookup"><span data-stu-id="09a41-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="09a41-123">Vá para **políticas locais** e abra **atribuição de direitos de usuário**.</span><span class="sxs-lookup"><span data-stu-id="09a41-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="09a41-124">Selecione **fazer logon como um trabalho em lotes** e adicione a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="09a41-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="09a41-125">O valor **runas** não é usado para servidores configurados para serem executados como serviços.</span><span class="sxs-lookup"><span data-stu-id="09a41-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="09a41-126">Os serviços COM que precisam ser executados com uma identidade diferente do LocalSystem devem definir o nome de usuário e a senha apropriados usando o miniaplicativo serviços do painel de controle ou as funções do controlador de serviço.</span><span class="sxs-lookup"><span data-stu-id="09a41-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="09a41-127">(Para obter mais informações sobre essas funções, consulte [Serviços](/windows/desktop/Services/services).)</span><span class="sxs-lookup"><span data-stu-id="09a41-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="09a41-128">A partir do Microsoft Windows Server 2003, a classe AppID é lida explicitamente a partir do **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID**, que, ao contrário da maioria das chaves do registro, não é intercambiável com a **\_ \_ \\ AppID raiz das classes hKey**.</span><span class="sxs-lookup"><span data-stu-id="09a41-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="09a41-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09a41-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a41-130">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="09a41-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 