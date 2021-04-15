---
title: EnableDCOM
description: Controla a ativação global e as políticas de chamada do computador. Somente administradores e o sistema têm acesso total a essa parte do registro. Todos os outros usuários têm acesso somente leitura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- COM valor do registro EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363844"
---
# <a name="enabledcom"></a><span data-ttu-id="a2e63-106">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="a2e63-106">EnableDCOM</span></span>

<span data-ttu-id="a2e63-107">Controla a ativação global e as políticas de chamada do computador.</span><span class="sxs-lookup"><span data-stu-id="a2e63-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="a2e63-108">Somente administradores e o sistema têm acesso total a essa parte do registro.</span><span class="sxs-lookup"><span data-stu-id="a2e63-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="a2e63-109">Todos os outros usuários têm acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a2e63-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a2e63-110">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="a2e63-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="a2e63-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2e63-111">Remarks</span></span>

<span data-ttu-id="a2e63-112">Este é um valor de **\_ sz do reg** .</span><span class="sxs-lookup"><span data-stu-id="a2e63-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="a2e63-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a2e63-113">Value</span></span>    | <span data-ttu-id="a2e63-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2e63-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e63-115">N (ou n)</span><span class="sxs-lookup"><span data-stu-id="a2e63-115">N (or n)</span></span> | <span data-ttu-id="a2e63-116">Nenhum cliente remoto pode iniciar servidores ou conectar-se a objetos neste computador.</span><span class="sxs-lookup"><span data-stu-id="a2e63-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="a2e63-117">Os clientes locais não podem acessar servidores DCOM remotos; todo o tráfego DCOM está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a2e63-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="a2e63-118">A inicialização local do código de classe e a conexão a objetos são permitidas por classe, de acordo com o valor e as permissões de acesso do valor do registro [**LaunchPermission**](launchpermission.md) da classe e o valor do registro global [**DefaultLaunchPermission**](defaultlaunchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="a2e63-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="a2e63-119">Y (ou y)</span><span class="sxs-lookup"><span data-stu-id="a2e63-119">Y (or y)</span></span> | <span data-ttu-id="a2e63-120">A inicialização de servidores e a conexão a objetos por clientes remotos é permitida por classe, de acordo com o valor e as permissões de acesso do valor do registro [**LaunchPermission**](launchpermission.md) da classe e o valor do registro global [**DefaultLaunchPermission**](defaultlaunchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="a2e63-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a2e63-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2e63-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2e63-122">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="a2e63-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="a2e63-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="a2e63-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="a2e63-124">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="a2e63-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




