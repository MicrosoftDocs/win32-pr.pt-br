---
description: Se você optar por implementar o apagamento em seu aplicativo que não seja usando o objeto InkOverlay, poderá fazer isso usando um dos dois métodos a seguir.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Apagando usando a caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370651"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="9a070-103">Apagando usando a caneta</span><span class="sxs-lookup"><span data-stu-id="9a070-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="9a070-104">Se você optar por implementar o apagamento em seu aplicativo que não seja usando o objeto [**InkOverlay**](inkoverlay-class.md) , poderá fazer isso usando um dos dois métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a070-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="9a070-105">Usando a ponta da caneta</span><span class="sxs-lookup"><span data-stu-id="9a070-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="9a070-106">A ponta da caneta eletrônica geralmente é usada para manuscrito e desenho; no entanto, a dica também pode ser usada para apagar a tinta.</span><span class="sxs-lookup"><span data-stu-id="9a070-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="9a070-107">Para fazer isso, o aplicativo deve ter um modo de apagamento que os usuários podem empregar.</span><span class="sxs-lookup"><span data-stu-id="9a070-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="9a070-108">Nesse modo, use o teste de clique para determinar a tinta que o cursor está movendo.</span><span class="sxs-lookup"><span data-stu-id="9a070-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="9a070-109">Você pode definir o modo de apagamento para excluir apenas a tinta que o cursor passa ou traços inteiros que interseccionam o caminho do cursor, dependendo do design ou das considerações funcionais.</span><span class="sxs-lookup"><span data-stu-id="9a070-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="9a070-110">Para obter um exemplo de como usar um modo de apagamento para apagar a tinta, consulte o [exemplo de apagamento de tinta](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9a070-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="9a070-111">Usando a parte superior da caneta</span><span class="sxs-lookup"><span data-stu-id="9a070-111">Using the Top of the Pen</span></span>

<span data-ttu-id="9a070-112">Para implementar o apagamento com a parte superior da caneta do Tablet, seu aplicativo deve procurar uma alteração no cursor.</span><span class="sxs-lookup"><span data-stu-id="9a070-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="9a070-113">Para procurar o cursor invertido, ouça o evento [**CursorInRange**](inkoverlay-cursorinrange.md) para determinar quando o cursor está dentro do contexto do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a070-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="9a070-114">Quando o cursor estiver no intervalo, procure a propriedade [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) no objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="9a070-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="9a070-115">Se a propriedade **invertida** for **true**, execute o teste de clique para determinar a tinta que o cursor está movendo.</span><span class="sxs-lookup"><span data-stu-id="9a070-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="9a070-116">Apague a tinta ou os traços que interseccionam o caminho do cursor, dependendo do design ou das considerações funcionais.</span><span class="sxs-lookup"><span data-stu-id="9a070-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="9a070-117">Para obter um exemplo de como usar a parte superior da caneta para apagar a tinta, consulte o [exemplo de apagamento de tinta](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9a070-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="9a070-118">Determinando se o apagamento com a parte superior da caneta está habilitado</span><span class="sxs-lookup"><span data-stu-id="9a070-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="9a070-119">Os usuários podem usar o topo da caneta para apagar a tinta em aplicativos criados para Tablet PC, se o hardware específico permitir.</span><span class="sxs-lookup"><span data-stu-id="9a070-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="9a070-120">Essa funcionalidade é acessada por uma caixa de seleção na caixa de grupo botões de caneta na guia Opções de caneta do diálogo painel de controle configurações de Tablet e caneta.</span><span class="sxs-lookup"><span data-stu-id="9a070-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="9a070-121">Para detectar se o usuário ativou o apagamento para a parte superior da caneta, verifique a seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="9a070-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="9a070-122">A `EraseEnable` entrada dessa subchave é do tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="9a070-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="9a070-123">O valor dessa entrada é 1 para habilitado, ou 0 para desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9a070-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="9a070-124">Outros valores são reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9a070-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="9a070-125">Se seu aplicativo permitir que a parte superior da caneta seja usada para apagar, você deverá verificar e armazenar em cache o valor da entrada EraseEnable quando:</span><span class="sxs-lookup"><span data-stu-id="9a070-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="9a070-126">O aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="9a070-126">Your application launches.</span></span>
-   <span data-ttu-id="9a070-127">Sempre que seu aplicativo receber o foco depois de perder o foco.</span><span class="sxs-lookup"><span data-stu-id="9a070-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="9a070-128">Use esse valor em cache para modificar o comportamento do seu aplicativo adequadamente.</span><span class="sxs-lookup"><span data-stu-id="9a070-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="9a070-129">O exemplo C a seguir \# define um `GetEraseEnabled` método que verifica o valor da `EraseEnable` entrada da `SysEventParameters` subchave.</span><span class="sxs-lookup"><span data-stu-id="9a070-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="9a070-130">O `GetEraseEnabled` método retornará **true** se o valor da entrada for 1; retornará **false** se o valor da entrada for 0; ou lançar uma exceção [InvalidOperationException](/dotnet/api/system.invalidoperationexception) se o valor da entrada for diferente de 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="9a070-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="9a070-131">O `GetEraseEnabled` método retornará o valor esperado **true** se a subchave ou a entrada não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="9a070-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
