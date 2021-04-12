---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina se o RPCSs acrescenta automaticamente um \_ \_ Sid de todos os pacotes de aplicativos a restrições com por padrão.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363726"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a><span data-ttu-id="36fe9-103">DoNotAddAllApplicationPackagesToRestrictions</span><span class="sxs-lookup"><span data-stu-id="36fe9-103">DoNotAddAllApplicationPackagesToRestrictions</span></span>

<span data-ttu-id="36fe9-104">Determina se o RPCSs acrescenta automaticamente um \_ \_ Sid de todos os pacotes de aplicativos a restrições com por padrão.</span><span class="sxs-lookup"><span data-stu-id="36fe9-104">Determines whether RPCSS automatically appends an ALL\_APPLICATION\_PACKAGES SID to COM restrictions by default.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="36fe9-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="36fe9-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a><span data-ttu-id="36fe9-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="36fe9-106">Remarks</span></span>

<span data-ttu-id="36fe9-107">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="36fe9-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="36fe9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="36fe9-108">Value</span></span> | <span data-ttu-id="36fe9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="36fe9-109">Description</span></span>                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="36fe9-110">0</span><span class="sxs-lookup"><span data-stu-id="36fe9-110">0</span></span>     | <span data-ttu-id="36fe9-111">Desabilita os aplicativos da Windows Store após a migração do Windows 7 para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="36fe9-111">Disables Windows Store apps upon migration from Windows 7 to Windows 8.</span></span>                   |
| <span data-ttu-id="36fe9-112">1</span><span class="sxs-lookup"><span data-stu-id="36fe9-112">1</span></span>     | <span data-ttu-id="36fe9-113">Não adiciona o SID todos \_ os \_ pacotes de aplicativos a restrições com.</span><span class="sxs-lookup"><span data-stu-id="36fe9-113">Does not add the ALL\_APPLICATION\_PACKAGES SID to COM restrictions.</span></span> <span data-ttu-id="36fe9-114">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="36fe9-114">This is the default.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="36fe9-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36fe9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36fe9-116">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="36fe9-116">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




