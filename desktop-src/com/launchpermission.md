---
title: LaunchPermission
description: Descreve a lista de controle de acesso (ACL) das entidades de segurança que podem iniciar novos servidores para essa classe. Esse valor pode ser adicionado sob qualquer chave AppID para limitar a ativação por clientes remotos de classes específicas.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- COM valor do registro LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006169"
---
# <a name="launchpermission"></a><span data-ttu-id="dded4-105">LaunchPermission</span><span class="sxs-lookup"><span data-stu-id="dded4-105">LaunchPermission</span></span>

<span data-ttu-id="dded4-106">Descreve a lista de controle de acesso (ACL) das entidades de segurança que podem iniciar novos servidores para essa classe.</span><span class="sxs-lookup"><span data-stu-id="dded4-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="dded4-107">Esse valor pode ser adicionado sob qualquer chave [**AppID**](appid-key.md) para limitar a ativação por clientes remotos de classes específicas.</span><span class="sxs-lookup"><span data-stu-id="dded4-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="dded4-108">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="dded4-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="dded4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="dded4-109">Remarks</span></span>

<span data-ttu-id="dded4-110">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="dded4-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="dded4-111">Após o recebimento de uma solicitação local ou remota para iniciar o servidor dessa classe, a ACL descrita por esse valor é verificada ao representar o cliente e seu sucesso permite ou não a inicialização do servidor.</span><span class="sxs-lookup"><span data-stu-id="dded4-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="dded4-112">Se esse valor não existir, o valor de [**DefaultLaunchPermission**](defaultlaunchpermission.md) será verificado da mesma maneira para determinar se o código de classe pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="dded4-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dded4-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dded4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dded4-114">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="dded4-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="dded4-115">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="dded4-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="dded4-116">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="dded4-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




