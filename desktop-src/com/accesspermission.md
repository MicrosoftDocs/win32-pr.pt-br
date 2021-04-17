---
title: AccessPermission
description: Descreve a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe. Essa ACL é usada somente por aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- COM valor do registro AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454361"
---
# <a name="accesspermission"></a><span data-ttu-id="bc41a-105">AccessPermission</span><span class="sxs-lookup"><span data-stu-id="bc41a-105">AccessPermission</span></span>

<span data-ttu-id="bc41a-106">Descreve a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="bc41a-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="bc41a-107">Essa ACL é usada somente por aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="bc41a-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="bc41a-108">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="bc41a-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="bc41a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc41a-109">Remarks</span></span>

<span data-ttu-id="bc41a-110">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="bc41a-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="bc41a-111">Ele contém dados que descrevem a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="bc41a-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="bc41a-112">Após receber uma solicitação para se conectar a um objeto existente dessa classe, a ACL é verificada pelo aplicativo que está sendo chamado ao representar o chamador.</span><span class="sxs-lookup"><span data-stu-id="bc41a-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="bc41a-113">Se a verificação de acesso falhar, a conexão não será permitida.</span><span class="sxs-lookup"><span data-stu-id="bc41a-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="bc41a-114">Se esse valor nomeado não existir, a ACL [**DefaultAccessPermission**](defaultaccesspermission.md) será testada para determinar se a conexão deve ser permitida.</span><span class="sxs-lookup"><span data-stu-id="bc41a-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="bc41a-115">Para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou não usam a interface [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar a AppID, o executável do binário do aplicativo deve ser mapeado para a AppID do aplicativo, conforme descrito em [**AppID**](appid.md).</span><span class="sxs-lookup"><span data-stu-id="bc41a-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="bc41a-116">Isso é necessário para que o COM possa localizar a AppID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc41a-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc41a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc41a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc41a-118">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="bc41a-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="bc41a-119">**DefaultAccessPermission**</span><span class="sxs-lookup"><span data-stu-id="bc41a-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="bc41a-120">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="bc41a-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 