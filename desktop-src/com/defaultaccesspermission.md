---
title: DefaultAccessPermission
description: Define a ACL (lista de controle de acesso) das entidades de segurança que podem acessar classes para as quais não há nenhuma configuração AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- COM valor do registro DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796144"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="4b36d-104">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="4b36d-104">DefaultAccessPermission</span></span>

<span data-ttu-id="4b36d-105">Define a ACL (lista de controle de acesso) das entidades de segurança que podem acessar classes para as quais não há nenhuma configuração [**AccessPermission**](accesspermission.md) .</span><span class="sxs-lookup"><span data-stu-id="4b36d-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="4b36d-106">Essa ACL é usada somente por aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e não têm um valor **AccessPermission** sob sua chave [**AppID**](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="4b36d-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="4b36d-107">Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="4b36d-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="4b36d-108">Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico.</span><span class="sxs-lookup"><span data-stu-id="4b36d-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="4b36d-109">Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="4b36d-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="4b36d-110">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="4b36d-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="4b36d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b36d-111">Remarks</span></span>

<span data-ttu-id="4b36d-112">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="4b36d-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="4b36d-113">O tempo de execução COM no servidor verifica a ACL descrita por esse valor ao representar o chamador que está tentando se conectar ao objeto e seu sucesso determina se o acesso é permitido ou não.</span><span class="sxs-lookup"><span data-stu-id="4b36d-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="4b36d-114">Se a verificação de acesso falhar, a conexão com o objeto não será permitida.</span><span class="sxs-lookup"><span data-stu-id="4b36d-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="4b36d-115">Se esse valor nomeado não existir, somente a entidade de segurança do servidor e o sistema local terão permissão para chamar o servidor.</span><span class="sxs-lookup"><span data-stu-id="4b36d-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="4b36d-116">Por padrão, esse valor não tem entradas nele.</span><span class="sxs-lookup"><span data-stu-id="4b36d-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="4b36d-117">Somente a entidade de segurança do servidor e o sistema têm permissão para chamar o servidor.</span><span class="sxs-lookup"><span data-stu-id="4b36d-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="4b36d-118">Esse valor fornece um nível simples de administração centralizada do acesso de conexão padrão à execução de objetos em um computador.</span><span class="sxs-lookup"><span data-stu-id="4b36d-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b36d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b36d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b36d-120">**AccessPermission**</span><span class="sxs-lookup"><span data-stu-id="4b36d-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="4b36d-121">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="4b36d-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="4b36d-122">Definindo a segurança de todo o processo</span><span class="sxs-lookup"><span data-stu-id="4b36d-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




