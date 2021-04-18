---
description: Acessando um valor de registro sem nome
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Acessando um valor de registro sem nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786244"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="1558d-103">Acessando um valor de registro sem nome</span><span class="sxs-lookup"><span data-stu-id="1558d-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="1558d-104">O valor padrão ou não nomeado de uma chave do registro é mostrado como (padrão) ou <No Name> no editor do registro do regedit.</span><span class="sxs-lookup"><span data-stu-id="1558d-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="1558d-105">Você pode usar o provedor de registro do sistema para acessar uma chave de registro sem nome.</span><span class="sxs-lookup"><span data-stu-id="1558d-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="1558d-106">Da mesma forma, você também pode usar o provedor de registro do sistema para acessar descrições de bitmap, que são definidas como valores não nomeados.</span><span class="sxs-lookup"><span data-stu-id="1558d-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="1558d-107">O procedimento a seguir descreve como recuperar um valor de registro sem nome.</span><span class="sxs-lookup"><span data-stu-id="1558d-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="1558d-108">**Para recuperar um valor de registro sem nome**</span><span class="sxs-lookup"><span data-stu-id="1558d-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="1558d-109">Defina uma propriedade e defina o qualificador **PropertyContext** dessa propriedade como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="1558d-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="1558d-110">O exemplo de código a seguir mostra como a classe define propriedades para armazenar valores para a chave especificada pelo qualificador **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="1558d-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="1558d-111">O valor padrão é armazenado na propriedade **padrão** .</span><span class="sxs-lookup"><span data-stu-id="1558d-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="1558d-112">A chave de transportes não usa o valor sem nome, portanto, a compilação desse arquivo MOF não produz nenhum valor para a propriedade **padrão** , a menos que uma ferramenta de edição de registro seja usada para alterar o valor sem nome.</span><span class="sxs-lookup"><span data-stu-id="1558d-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="1558d-113">Para um arquivo de bitmap, defina uma propriedade e defina o **PropertyContext** dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1558d-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="1558d-114">O exemplo de código a seguir mostra como definir uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="1558d-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



