---
title: DefaultLaunchPermission
description: Define a ACL (lista de controle de acesso) das entidades de segurança que podem iniciar classes que não especificam sua própria ACL por meio do valor do registro LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- COM valor do registro DefaultLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811659"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="4d063-104">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="4d063-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="4d063-105">Define a ACL (lista de controle de acesso) das entidades de segurança que podem iniciar classes que não especificam sua própria ACL por meio do valor do registro [**LaunchPermission**](launchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="4d063-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="4d063-106">Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="4d063-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="4d063-107">Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico.</span><span class="sxs-lookup"><span data-stu-id="4d063-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="4d063-108">Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="4d063-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="4d063-109">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="4d063-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="4d063-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d063-110">Remarks</span></span>

<span data-ttu-id="4d063-111">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="4d063-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="4d063-112">As permissões de acesso padrão são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="4d063-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="4d063-113">Administradores: permitir inicialização</span><span class="sxs-lookup"><span data-stu-id="4d063-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="4d063-114">SISTEMA: permitir inicialização</span><span class="sxs-lookup"><span data-stu-id="4d063-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="4d063-115">INTERATIVO: permitir inicialização</span><span class="sxs-lookup"><span data-stu-id="4d063-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="4d063-116">Se o valor de [**LaunchPermission**](launchpermission.md) for definido para um servidor, ele terá precedência sobre o valor de **DefaultLaunchPermission** .</span><span class="sxs-lookup"><span data-stu-id="4d063-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="4d063-117">Ao receber uma solicitação local ou remota para iniciar um servidor cuja chave [**AppID**](appid-key.md) não tem nenhum valor **LaunchPermission** próprio, a ACL descrita por esse valor é verificada ao representar o cliente e seu sucesso permite ou não a inicialização do código de classe.</span><span class="sxs-lookup"><span data-stu-id="4d063-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="4d063-118">Esse valor fornece um nível simples de administração centralizada do acesso de inicialização padrão a classes não administradas de outra forma em um computador.</span><span class="sxs-lookup"><span data-stu-id="4d063-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="4d063-119">Por exemplo, um administrador pode usar a ferramenta DCOMCNFG para configurar o sistema para permitir o acesso somente leitura para usuários avançados.</span><span class="sxs-lookup"><span data-stu-id="4d063-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="4d063-120">Portanto, o OLE restringiria as solicitações para iniciar o código de classe para membros do grupo usuários avançados.</span><span class="sxs-lookup"><span data-stu-id="4d063-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="4d063-121">Um administrador pode, subsequentemente, configurar permissões de inicialização para classes individuais para conceder a capacidade de iniciar o código de classe para outros grupos ou usuários individuais, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="4d063-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d063-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d063-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d063-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="4d063-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="4d063-124">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="4d063-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="4d063-125">Definindo a segurança de todo o processo</span><span class="sxs-lookup"><span data-stu-id="4d063-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




