---
description: Um usuário pode especificar as configurações de documento padrão para uma impressora. Isso é chamado de DEVMODE por usuário porque só afeta os padrões para um usuário específico, e as informações para cada impressora são definidas em uma estrutura DEVMODE separada.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791554"
---
# <a name="per-user-devmode"></a><span data-ttu-id="07010-104">Per-User DEVMODE</span><span class="sxs-lookup"><span data-stu-id="07010-104">Per-User DEVMODE</span></span>

<span data-ttu-id="07010-105">Um usuário pode especificar as configurações de documento padrão para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="07010-105">A user can specify the default document settings for a printer.</span></span> <span data-ttu-id="07010-106">Isso é chamado de *DEVMODE por usuário* porque só afeta os padrões para um usuário específico, e as informações para cada impressora são definidas em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) separada.</span><span class="sxs-lookup"><span data-stu-id="07010-106">This is called the *per-user DEVMODE* because it only affects the defaults for a particular user, and the information for each printer is defined in a separate [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

<span data-ttu-id="07010-107">Para definir o DEVMODE por usuário, chame [**Setprinter**](setprinter.md) com as informações da [**impressora \_ \_ 2**](printer-info-2.md) ou a estrutura [**\_ info \_ 9 da impressora**](printer-info-9.md) .</span><span class="sxs-lookup"><span data-stu-id="07010-107">To set the per-user DEVMODE, call [**SetPrinter**](setprinter.md) with either the [**PRINTER\_INFO\_2**](printer-info-2.md) or the [**PRINTER\_INFO\_9**](printer-info-9.md) structure.</span></span> <span data-ttu-id="07010-108">Para redefinir o DEVMODE por usuário para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)padrão global, chame **setprinter** com a estrutura [**informações da impressora \_ \_ 8**](printer-info-8.md) .</span><span class="sxs-lookup"><span data-stu-id="07010-108">To reset the per-user DEVMODE to the global default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), call **SetPrinter** with the [**PRINTER\_INFO\_8**](printer-info-8.md) structure.</span></span>

 

 



