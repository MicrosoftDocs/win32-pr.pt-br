---
title: Registrando uma DLL de segurança RAS
description: O programa de instalação para uma DLL de segurança RAS deve registrar a DLL com o servidor RAS do Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635688"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="d648f-103">Registrando uma DLL de segurança RAS</span><span class="sxs-lookup"><span data-stu-id="d648f-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="d648f-104">O programa de instalação para uma DLL de segurança RAS deve registrar a DLL com o servidor RAS do Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d648f-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="d648f-105">Somente uma DLL de segurança RAS pode ser registrada como suporte para várias DLLs de segurança não é fornecida.</span><span class="sxs-lookup"><span data-stu-id="d648f-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="d648f-106">Para registrar uma DLL de segurança de RAS, defina o valor de *DLLPath* sob a seguinte chave no registro:</span><span class="sxs-lookup"><span data-stu-id="d648f-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="d648f-107">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="d648f-107">Value name</span></span> | <span data-ttu-id="d648f-108">Dados do valor</span><span class="sxs-lookup"><span data-stu-id="d648f-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d648f-109">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="d648f-109">*DLLPath*</span></span>  | <span data-ttu-id="d648f-110">Uma cadeia de caracteres **reg \_ sz** que contém o caminho da dll.</span><span class="sxs-lookup"><span data-stu-id="d648f-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="d648f-111">Essa cadeia de caracteres deve especificar o caminho completo, a menos que a DLL esteja em um diretório listado no caminho do sistema.</span><span class="sxs-lookup"><span data-stu-id="d648f-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="d648f-112">O programa de instalação para uma DLL de segurança de RAS também deve fornecer a funcionalidade de remoção/desinstalação.</span><span class="sxs-lookup"><span data-stu-id="d648f-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="d648f-113">Se um usuário remover a DLL, o programa de instalação deverá excluir o valor de *DLLPath* do registro.</span><span class="sxs-lookup"><span data-stu-id="d648f-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="d648f-114">O serviço RAS não será iniciado se o valor de *DLLPath* especificar uma DLL que não pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="d648f-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="d648f-115">Uma DLL de segurança RAS deve exportar as funções [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) e [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .</span><span class="sxs-lookup"><span data-stu-id="d648f-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




