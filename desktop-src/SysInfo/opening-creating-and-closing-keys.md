---
description: Antes que um aplicativo possa adicionar dados ao registro, ele deve criar ou abrir uma chave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Abrindo, criando e fechando chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751057"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="5ccaa-103">Abrindo, criando e fechando chaves</span><span class="sxs-lookup"><span data-stu-id="5ccaa-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="5ccaa-104">Antes que um aplicativo possa adicionar dados ao registro, ele deve criar ou abrir uma chave.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="5ccaa-105">Para criar ou abrir uma chave, um aplicativo sempre se refere à chave como uma subchave de uma chave aberta no momento.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="5ccaa-106">As seguintes chaves predefinidas são sempre abertas: **HKEY \_ local \_ Machine**, **HKEY \_ classes \_ root**, **HKEY \_ Users** e **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="5ccaa-107">Um aplicativo usa a função [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) para abrir uma chave e a função [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) para criar uma chave.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="5ccaa-108">Uma árvore do registro pode ter 512 níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="5ccaa-109">Você pode criar até 32 níveis por vez por meio de uma única chamada à API do registro.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="5ccaa-110">Um aplicativo pode usar a função [**falha RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) para fechar uma chave e gravar os dados que ela contém no registro.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="5ccaa-111">O **falha RegCloseKey** não grava necessariamente os dados no registro antes de retornar; pode levar até vários segundos para que o cache seja liberado para o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="5ccaa-112">Se um aplicativo precisar gravar dados de registro explicitamente no disco rígido, ele poderá usar a função [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) .</span><span class="sxs-lookup"><span data-stu-id="5ccaa-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="5ccaa-113">O **RegFlushKey**, no entanto, usa muitos recursos do sistema e deve ser chamado somente quando absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



