---
description: Explica como criar um controle de entrada matemática.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Criando um controle de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567028"
---
# <a name="creating-a-math-input-control"></a><span data-ttu-id="a71b8-103">Criando um controle de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="a71b8-103">Creating a Math Input Control</span></span>

<span data-ttu-id="a71b8-104">Para criar o controle de entrada de matemática, você deve:</span><span class="sxs-lookup"><span data-stu-id="a71b8-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="a71b8-105">Incluir cabeçalhos e bibliotecas para o controle de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="a71b8-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="a71b8-106">Declare o ponteiro de controle e chame CoInitialize no ponteiro de controle</span><span class="sxs-lookup"><span data-stu-id="a71b8-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="a71b8-107">Mostrar o controle</span><span class="sxs-lookup"><span data-stu-id="a71b8-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="a71b8-108">Incluir cabeçalhos e bibliotecas para o controle de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="a71b8-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="a71b8-109">O código a seguir deve ser colocado na parte superior do seu código, em que você usará o controle de entrada de matemática.</span><span class="sxs-lookup"><span data-stu-id="a71b8-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="a71b8-110">Esse código adicionará suporte para o controle de entrada matemática para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a71b8-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="a71b8-111">Declare o ponteiro de controle e chame CoInitialize no ponteiro de controle</span><span class="sxs-lookup"><span data-stu-id="a71b8-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="a71b8-112">Depois de incluir os cabeçalhos para seu controle, você pode declarar o ponteiro de controle e pode chamar CoInitialize nele para criar um identificador para a interface de controle de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="a71b8-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="a71b8-113">O código a seguir pode ser colocado em uma classe ou como uma variável global na implementação do seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="a71b8-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="a71b8-114">O código a seguir mostra como você pode chamar CoInitialize no ponteiro de controle.</span><span class="sxs-lookup"><span data-stu-id="a71b8-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="a71b8-115">Depois de chamar o CoInitialize no ponteiro de controle, você tem uma referência ao controle e pode acessar os métodos do controle.</span><span class="sxs-lookup"><span data-stu-id="a71b8-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="a71b8-116">Por exemplo, você pode habilitar o conjunto estendido de controles, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a71b8-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="a71b8-117">Mostrar o controle</span><span class="sxs-lookup"><span data-stu-id="a71b8-117">Show the Control</span></span>

<span data-ttu-id="a71b8-118">O controle não será exibido automaticamente depois que você criá-lo.</span><span class="sxs-lookup"><span data-stu-id="a71b8-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="a71b8-119">Para mostrar o controle, chame o método [**show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) na referência de controle que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="a71b8-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="a71b8-120">O código a seguir demonstra como o método [**show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="a71b8-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="a71b8-121">Depois que o controle for exibido, ele será semelhante à ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a71b8-121">After the control shows, it will look something like the following illustration.</span></span>

![captura de tela mostrando o controle de entrada matemática](images/mic.png)

<span data-ttu-id="a71b8-123">Observe que habilitei o conjunto estendido de botões para que **refazer** e **desfazer** estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a71b8-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
