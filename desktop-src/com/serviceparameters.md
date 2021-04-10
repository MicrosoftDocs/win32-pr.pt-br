---
title: Serviceparameters
description: Especifica os parâmetros de linha de comando a serem passados para um objeto instalado para uso pelo COM por meio do valor do registro LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- COM valor de registro serviceparameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292230"
---
# <a name="serviceparameters"></a><span data-ttu-id="e4f82-104">Serviceparameters</span><span class="sxs-lookup"><span data-stu-id="e4f82-104">ServiceParameters</span></span>

<span data-ttu-id="e4f82-105">Especifica os parâmetros de linha de comando a serem passados para um objeto instalado para uso pelo COM por meio do valor do registro [**LocalService**](localservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f82-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e4f82-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="e4f82-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="e4f82-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4f82-107">Remarks</span></span>

<span data-ttu-id="e4f82-108">Este é um valor de **\_ sz do reg** .</span><span class="sxs-lookup"><span data-stu-id="e4f82-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="e4f82-109">Essa cadeia de caracteres é passada para o serviço como um argumento de linha de comando à medida que ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e4f82-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4f82-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4f82-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f82-111">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="e4f82-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="e4f82-112">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="e4f82-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




