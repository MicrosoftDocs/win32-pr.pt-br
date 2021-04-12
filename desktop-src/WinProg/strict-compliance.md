---
title: Conformidade estrita
description: Um código-fonte que compila com êxito pode produzir mensagens de erro quando você habilita a verificação de tipo estrito.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366277"
---
# <a name="strict-compliance"></a><span data-ttu-id="6d72e-103">Conformidade estrita</span><span class="sxs-lookup"><span data-stu-id="6d72e-103">STRICT Compliance</span></span>

<span data-ttu-id="6d72e-104">Um código-fonte que compila com êxito pode produzir mensagens de erro quando você habilita a verificação de tipo **estrito** .</span><span class="sxs-lookup"><span data-stu-id="6d72e-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="6d72e-105">As seções a seguir descrevem os requisitos mínimos para fazer com que seu código seja compilado quando **Strict** estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="6d72e-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="6d72e-106">Etapas adicionais são recomendadas, especialmente para produzir código portátil.</span><span class="sxs-lookup"><span data-stu-id="6d72e-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="6d72e-107">Requisitos gerais</span><span class="sxs-lookup"><span data-stu-id="6d72e-107">General Requirements</span></span>

<span data-ttu-id="6d72e-108">O requisito principal é que você deve declarar tipos de identificador e ponteiros de função corretos em vez de depender de tipos mais gerais.</span><span class="sxs-lookup"><span data-stu-id="6d72e-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="6d72e-109">Você não pode usar um tipo de identificador em que outro é esperado.</span><span class="sxs-lookup"><span data-stu-id="6d72e-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="6d72e-110">Isso também significa que você pode precisar alterar as declarações de função e usar mais conversões de tipo.</span><span class="sxs-lookup"><span data-stu-id="6d72e-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="6d72e-111">Para obter melhores resultados, o tipo de **identificador** genérico deve ser usado somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="6d72e-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="6d72e-112">Declarando funções dentro de seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="6d72e-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="6d72e-113">Verifique se todas as funções de aplicativo estão declaradas.</span><span class="sxs-lookup"><span data-stu-id="6d72e-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="6d72e-114">É recomendável colocar todas as declarações de função em um arquivo de inclusão, pois você pode facilmente examinar suas declarações e procurar os tipos de parâmetro e de retorno que devem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="6d72e-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="6d72e-115">Se você usar a opção de compilador **/ZG** para criar arquivos de cabeçalho para suas funções, lembre-se de que obterá resultados diferentes dependendo se você tiver habilitado a verificação de tipo **estrito** .</span><span class="sxs-lookup"><span data-stu-id="6d72e-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="6d72e-116">Com **Strict** Disabled, todos os tipos de identificador geram o mesmo tipo base.</span><span class="sxs-lookup"><span data-stu-id="6d72e-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="6d72e-117">Com o **Strict** Enabled, eles geram tipos de base diferentes.</span><span class="sxs-lookup"><span data-stu-id="6d72e-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="6d72e-118">Para evitar conflitos, você precisa recriar o arquivo de cabeçalho sempre que habilitar ou desabilitar **estrito**, ou editar o arquivo de cabeçalho para usar os tipos **HWND**, **HDC**, **Handle** e assim por diante, em vez dos tipos base.</span><span class="sxs-lookup"><span data-stu-id="6d72e-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="6d72e-119">Qualquer declaração de função que você copiou do Windows. h para o código-fonte pode ter sido alterada e sua declaração local pode estar desatualizada.</span><span class="sxs-lookup"><span data-stu-id="6d72e-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="6d72e-120">Remova sua declaração local.</span><span class="sxs-lookup"><span data-stu-id="6d72e-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="6d72e-121">Tipos que exigem conversões</span><span class="sxs-lookup"><span data-stu-id="6d72e-121">Types that Require Casts</span></span>

<span data-ttu-id="6d72e-122">Algumas funções têm tipos de retorno genéricos ou parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6d72e-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="6d72e-123">Por exemplo, a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) retorna dados que podem ser qualquer número de tipos, dependendo do contexto.</span><span class="sxs-lookup"><span data-stu-id="6d72e-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="6d72e-124">Quando você vir qualquer uma dessas funções em seu código-fonte, verifique se você usa a conversão de tipo correta e se ela é a mais específica possível.</span><span class="sxs-lookup"><span data-stu-id="6d72e-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="6d72e-125">A lista a seguir é um exemplo dessas funções.</span><span class="sxs-lookup"><span data-stu-id="6d72e-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="6d72e-126">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="6d72e-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="6d72e-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="6d72e-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="6d72e-128">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="6d72e-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="6d72e-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="6d72e-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="6d72e-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6d72e-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="6d72e-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6d72e-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="6d72e-132">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="6d72e-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="6d72e-133">Ao chamar [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)ou [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), você deve primeiro converter o resultado para o tipo **uint \_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="6d72e-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="6d72e-134">Você precisa tomar etapas semelhantes para qualquer função que retorne um valor **\_ PTR** **LRESULT** ou Long, em que o resultado contenha um identificador.</span><span class="sxs-lookup"><span data-stu-id="6d72e-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="6d72e-135">Isso é necessário para escrever código portátil porque o tamanho de um identificador varia, dependendo da versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d72e-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="6d72e-136">A conversão (**uint \_ PTR**) garante a conversões corretas.</span><span class="sxs-lookup"><span data-stu-id="6d72e-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="6d72e-137">O código a seguir mostra um exemplo em que **SendMessage** retorna um identificador para um pincel:</span><span class="sxs-lookup"><span data-stu-id="6d72e-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="6d72e-138">O parâmetro **CreateWindow** e **CreateWindowEx** *HMENU* às vezes é usado para passar um identificador de controle de inteiro (ID).</span><span class="sxs-lookup"><span data-stu-id="6d72e-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="6d72e-139">Nesse caso, você deve converter a ID para um tipo **HMENU** :</span><span class="sxs-lookup"><span data-stu-id="6d72e-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="6d72e-140">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="6d72e-140">Additional Considerations</span></span>

<span data-ttu-id="6d72e-141">Para aproveitar ao máximo o benefício da verificação de tipo **estrito** , há diretrizes adicionais que você deve seguir.</span><span class="sxs-lookup"><span data-stu-id="6d72e-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="6d72e-142">Seu código será mais portátil em versões futuras do Windows se você fizer as seguintes alterações.</span><span class="sxs-lookup"><span data-stu-id="6d72e-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="6d72e-143">Os tipos **wParam**, **lParam**, **LRESULT** e **LPVOID** são *tipos de dados polimórficos*.</span><span class="sxs-lookup"><span data-stu-id="6d72e-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="6d72e-144">Eles mantêm diferentes tipos de dados em momentos diferentes, mesmo quando a verificação de tipo **estrito** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6d72e-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="6d72e-145">Para obter o benefício da verificação de tipo, você deve converter valores desses tipos assim que possível.</span><span class="sxs-lookup"><span data-stu-id="6d72e-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="6d72e-146">(Observe que os decifradores de mensagens reconvertem automaticamente *wParam* e *lParam* para você de maneira portátil.)</span><span class="sxs-lookup"><span data-stu-id="6d72e-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="6d72e-147">Tome cuidado especial para distinguir os tipos **HMODULE** e **HINSTANCE** .</span><span class="sxs-lookup"><span data-stu-id="6d72e-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="6d72e-148">Mesmo com **Strict** Enabled, eles são definidos como o mesmo tipo base.</span><span class="sxs-lookup"><span data-stu-id="6d72e-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="6d72e-149">A maioria das funções de gerenciamento de módulo de kernel usa tipos **HINSTANCE** , mas há algumas funções que retornam ou aceitam apenas tipos **HMODULE** .</span><span class="sxs-lookup"><span data-stu-id="6d72e-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d72e-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d72e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d72e-151">Desabilitando estrito</span><span class="sxs-lookup"><span data-stu-id="6d72e-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="6d72e-152">Habilitando STRICT</span><span class="sxs-lookup"><span data-stu-id="6d72e-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 