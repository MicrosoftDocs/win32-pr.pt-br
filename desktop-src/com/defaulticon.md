---
title: DefaultIcon
description: Fornece informações de ícone padrão para icônico apresentações de objetos.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008419"
---
# <a name="defaulticon"></a><span data-ttu-id="69ca3-104">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="69ca3-104">DefaultIcon</span></span>

<span data-ttu-id="69ca3-105">Fornece informações de ícone padrão para icônico apresentações de objetos.</span><span class="sxs-lookup"><span data-stu-id="69ca3-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="69ca3-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="69ca3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="69ca3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="69ca3-107">Remarks</span></span>

<span data-ttu-id="69ca3-108">Esse é um valor **reg \_ sz** que especifica o caminho completo para o nome do executável do aplicativo de objeto e o índice de recursos do ícone no executável.</span><span class="sxs-lookup"><span data-stu-id="69ca3-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="69ca3-109">**DefaultIcon** identifica o ícone a ser usado quando, por exemplo, um controle é minimizado para um ícone.</span><span class="sxs-lookup"><span data-stu-id="69ca3-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="69ca3-110">Essa entrada contém o caminho completo para o nome do executável do aplicativo de servidor e o índice de recursos do ícone no executável.</span><span class="sxs-lookup"><span data-stu-id="69ca3-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="69ca3-111">Os aplicativos podem usar as informações fornecidas por **DefaultIcon** para obter um identificador de ícone com [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span><span class="sxs-lookup"><span data-stu-id="69ca3-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 