---
description: Descrição do uso do objeto PenInputPanel para programar o painel de entrada do Tablet PC no nível do sistema.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programando o painel de entrada usando a classe PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297527"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a><span data-ttu-id="db6ba-103">Programando o painel de entrada usando a classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="db6ba-103">Programming the Input Panel Using the PenInputPanel Class</span></span>

<span data-ttu-id="db6ba-104">\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="db6ba-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="db6ba-105">Consulte [programando o painel de entrada de texto](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="db6ba-105">Please refer to [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="db6ba-106">Descrição do uso do objeto [**PenInputPanel**](peninputpanel-class.md) para programar o painel de entrada do Tablet PC no nível do sistema.</span><span class="sxs-lookup"><span data-stu-id="db6ba-106">Description of using the [**PenInputPanel**](peninputpanel-class.md) object to program the system-level Tablet PC Input Panel.</span></span>

## <a name="input-panel-vs-the-peninputpanel-object"></a><span data-ttu-id="db6ba-107">Painel de entrada versus o objeto PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="db6ba-107">Input Panel vs. the PenInputPanel Object</span></span>

<span data-ttu-id="db6ba-108">No Microsoft Windows XP Tablet PC Edition versão 1,0, o painel de entrada do Tablet PC no nível do sistema fornece um mecanismo universal para realizar a entrada de texto na plataforma Windows, mas não fornece acesso programático.</span><span class="sxs-lookup"><span data-stu-id="db6ba-108">In Microsoft Windows XP Tablet PC Edition version 1.0, the system-level Tablet PC Input Panel provides a universal mechanism to accomplish text input across the Windows platform, but it does not provide programmatic access.</span></span> <span data-ttu-id="db6ba-109">No Windows XP Tablet PC Edition Software Development Kit (SDK) versão 1,5 e posterior, o objeto [**PenInputPanel**](peninputpanel-class.md) permite que você integre ferramentas de entrada de texto diretamente em seus aplicativos e forneça um nível de controle que não estava disponível anteriormente.</span><span class="sxs-lookup"><span data-stu-id="db6ba-109">In Windows XP Tablet PC Edition Software Development Kit (SDK) version 1.5 and later, the [**PenInputPanel**](peninputpanel-class.md) object enables you to integrate text input tools directly into your applications, and provide a level of control not previously available.</span></span> <span data-ttu-id="db6ba-110">A partir do Windows XP Tablet PC Edition 2005, o painel de entrada no nível do sistema foi atualizado para incluir a funcionalidade de entrada in-loco fornecida pelo objeto **PenInputPanel** e muito mais.</span><span class="sxs-lookup"><span data-stu-id="db6ba-110">Starting with the Windows XP Tablet PC Edition 2005, the system-level Input Panel has been upgraded to include the in-place input functionality provided by the **PenInputPanel** object and more.</span></span>

<span data-ttu-id="db6ba-111">O gráfico a seguir mostra o painel de entrada exibido sobre a amostra de [exemplo de formulário de declarações automática](auto-claims-form-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="db6ba-111">The following graphic shows Input Panel displayed over the [Auto Claims Form Sample](auto-claims-form-sample.md) sample.</span></span>

![painel de entrada exibido em um formulário usado para declarações de automóvel](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

<span data-ttu-id="db6ba-113">O painel de entrada substitui o [**PenInputPanel**](peninputpanel-class.md) fornecendo a mesma funcionalidade de entrada in-loco para qualquer aplicativo em execução no Windows XP Tablet PC Edition 2005 ou posterior sem a necessidade de código adicional.</span><span class="sxs-lookup"><span data-stu-id="db6ba-113">Input Panel supersedes the [**PenInputPanel**](peninputpanel-class.md) by supplying the same in-place input functionality to any application running on Windows XP Tablet PC Edition 2005 or later without the need for additional code.</span></span> <span data-ttu-id="db6ba-114">Este artigo sobre como usar o objeto **PenInputPanel** é fornecido para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="db6ba-114">This article on using the **PenInputPanel** object is provided for backward compatibility.</span></span> <span data-ttu-id="db6ba-115">Os aplicativos que já utilizam o objeto **PenInputPanel** funcionarão da mesma forma, exceto que o painel de entrada será exibido em vez do **PenInputPanel** quando o aplicativo for executado no Windows XP Tablet PC Edition 2005 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="db6ba-115">Applications that already utilize the **PenInputPanel** object will function the same except that Input Panel will be displayed instead of the **PenInputPanel** when the application is run on Windows XP Tablet PC Edition 2005 or later.</span></span>

<span data-ttu-id="db6ba-116">Se você estiver desenvolvendo um novo aplicativo para o Tablet PC e quiser ter uma solução de entrada do usuário in-loco, o painel de entrada fornecerá isso automaticamente no Windows XP Tablet PC Edition 2005 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="db6ba-116">If you are developing a new application for the Tablet PC and want to have an in-place user input solution, Input Panel provides this automatically on Windows XP Tablet PC Edition 2005 or later.</span></span> <span data-ttu-id="db6ba-117">Não é necessário criar uma instância do objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="db6ba-117">There is no need to instantiate the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

## <a name="disabling-the-input-panel"></a><span data-ttu-id="db6ba-118">Desabilitando o painel de entrada</span><span class="sxs-lookup"><span data-stu-id="db6ba-118">Disabling the Input Panel</span></span>

<span data-ttu-id="db6ba-119">Pode haver casos em que você deseja desabilitar o painel de entrada.</span><span class="sxs-lookup"><span data-stu-id="db6ba-119">There may be cases where you want to disable Input Panel.</span></span> <span data-ttu-id="db6ba-120">Há duas maneiras de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="db6ba-120">There are two ways to accomplish this.</span></span> <span data-ttu-id="db6ba-121">Você pode fazer isso programaticamente ou definindo uma entrada de registro que desabilita o painel de entrada para todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db6ba-121">You can accomplish this programmatically or by setting a registry entry that disables Input Panel for your entire application.</span></span>

### <a name="disabling-input-panel-programmatically"></a><span data-ttu-id="db6ba-122">Desabilitando o painel de entrada programaticamente</span><span class="sxs-lookup"><span data-stu-id="db6ba-122">Disabling Input Panel Programmatically</span></span>

<span data-ttu-id="db6ba-123">Para desabilitar o painel de entrada programaticamente, instancie o [**PenInputPanel**](peninputpanel-class.md) e defina sua propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) como **false**.</span><span class="sxs-lookup"><span data-stu-id="db6ba-123">To disable Input Panel programmatically, instantiate the [**PenInputPanel**](peninputpanel-class.md) and set its [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) property to **False**.</span></span>


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



<span data-ttu-id="db6ba-124">Para desabilitar o painel de entrada para vários controles em um único aplicativo, crie uma instância de um objeto [**PenInputPanel**](peninputpanel-class.md) para cada controle e defina a propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)como **false** para cada uma ou instancie um único **PenInputPanel** e mova-o de Control para Control como o foco de entrada é alterado.</span><span class="sxs-lookup"><span data-stu-id="db6ba-124">To disable Input Panel for multiple controls in a single application, either instantiate a [**PenInputPanel**](peninputpanel-class.md) object for each control and set the [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)property to **False** for each or instantiate a single **PenInputPanel** and move it from control to control as input focus changes.</span></span> <span data-ttu-id="db6ba-125">Para obter mais informações sobre essas duas técnicas, consulte o tópico de [exemplo PenInputPanel](peninputpanel-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="db6ba-125">For more information about these two techniques, see the [PenInputPanel Sample](peninputpanel-sample.md) topic.</span></span>

### <a name="disabling-input-panel-through-the-registry"></a><span data-ttu-id="db6ba-126">Desabilitando o painel de entrada por meio do registro</span><span class="sxs-lookup"><span data-stu-id="db6ba-126">Disabling Input Panel Through the Registry</span></span>

<span data-ttu-id="db6ba-127">Você pode definir uma entrada de registro para desabilitar o painel de entrada para todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db6ba-127">You can set a registry entry to disable Input Panel for your entire application.</span></span> <span data-ttu-id="db6ba-128">No entanto, isso também o desabilitará para caixas de diálogo comuns, como a caixa de diálogo **Abrir arquivo** , a caixa de diálogo **Imprimir** e a caixa de diálogo **salvar arquivo** .</span><span class="sxs-lookup"><span data-stu-id="db6ba-128">However, this will also disable it for common dialog boxes such as the **File Open** dialog box, the **Print** dialog box, and the **File Save** dialog box.</span></span> <span data-ttu-id="db6ba-129">Isso pode tornar a experiência do usuário em seu aplicativo inconsistente com outros aplicativos do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="db6ba-129">This may make the user experience in your application inconsistent with other Tablet PC applications.</span></span>

<span data-ttu-id="db6ba-130">Definir a `DisableInPlace` chave do registro como zero impede que a interface do usuário do painel de entrada seja exibida em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db6ba-130">Setting the `DisableInPlace` registry key to zero prevents Input Panel user interface (UI) from appearing in an application.</span></span> <span data-ttu-id="db6ba-131">Você deve posicionar a `DisableInPlace` chave do registro em `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` .</span><span class="sxs-lookup"><span data-stu-id="db6ba-131">You must place the `DisableInPlace` registry key at `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\`.</span></span> <span data-ttu-id="db6ba-132">Em seguida, adicione um novo valor de registro usando o caminho completo do aplicativo no qual você deseja desabilitar o painel de entrada.</span><span class="sxs-lookup"><span data-stu-id="db6ba-132">Then, add a new registry value by using the full path of the application in which you want to disable Input Panel.</span></span> <span data-ttu-id="db6ba-133">A seguinte entrada de registro de exemplo desabilita o painel de entrada em um aplicativo chamado MyApp:</span><span class="sxs-lookup"><span data-stu-id="db6ba-133">The following example registry entry disables Input Panel in an application called MyApp:</span></span>

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

<span data-ttu-id="db6ba-134">Se você ainda vir um problema em seu aplicativo depois de desabilitar a interface do usuário do painel de entrada, pode ser necessário desabilitar a estrutura subjacente, que consulta seu aplicativo para o local do cursor.</span><span class="sxs-lookup"><span data-stu-id="db6ba-134">If you still see a problem in your application after you disable the Input Panel UI, it may be necessary to disable the underlying framework, which queries your application for the caret location.</span></span> <span data-ttu-id="db6ba-135">Por exemplo, o painel de entrada pode expor um bug no código de rastreamento de cursor do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db6ba-135">For example, Input Panel may expose a bug in your application's caret tracking code.</span></span> <span data-ttu-id="db6ba-136">Desativar a consulta de rastreamento de cursor também impede que a interface do usuário do painel de entrada apareça.</span><span class="sxs-lookup"><span data-stu-id="db6ba-136">Turning off the caret tracking query also prevents the Input Panel UI from appearing.</span></span> <span data-ttu-id="db6ba-137">Para desabilitar a estrutura, defina a `EnableCaretTracking` chave do registro como zero.</span><span class="sxs-lookup"><span data-stu-id="db6ba-137">To disable the framework, set the `EnableCaretTracking` registry key to zero.</span></span> <span data-ttu-id="db6ba-138">Localize essa chave em `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .</span><span class="sxs-lookup"><span data-stu-id="db6ba-138">Locate this key at `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\`.</span></span>

> [!Note]  
> <span data-ttu-id="db6ba-139">Ferramentas de acessibilidade e tecnologia de fala no Windows XP também usam essa estrutura, portanto, desabilitar a consulta também desabilita esses recursos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db6ba-139">Accessibility tools and speech technology in Windows XP also use this framework, so disabling the query also disables these features in your application.</span></span>

 

## <a name="the-input-panel-and-web-pages"></a><span data-ttu-id="db6ba-140">O painel de entrada e as páginas da Web</span><span class="sxs-lookup"><span data-stu-id="db6ba-140">The Input Panel and Web Pages</span></span>

<span data-ttu-id="db6ba-141">Para usar uma API em uma página da Web, ela deve funcionar em um ambiente de confiança parcial.</span><span class="sxs-lookup"><span data-stu-id="db6ba-141">In order to use an API on a Web page, it must function in a partial trust environment.</span></span> <span data-ttu-id="db6ba-142">Todos os membros da classe [**PenInputPanel**](peninputpanel-class.md) exigem confiança total, exceto o seguinte:</span><span class="sxs-lookup"><span data-stu-id="db6ba-142">All [**PenInputPanel**](peninputpanel-class.md) class members require full trust except the following:</span></span>

-   <span data-ttu-id="db6ba-143">[Construtores PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (somente código gerenciado)</span><span class="sxs-lookup"><span data-stu-id="db6ba-143">[PenInputPanel Constructors](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (managed code only)</span></span>
-   <span data-ttu-id="db6ba-144">[Método Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (somente código gerenciado)</span><span class="sxs-lookup"><span data-stu-id="db6ba-144">[Dispose Method](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (managed code only)</span></span>
-   <span data-ttu-id="db6ba-145">[Propriedade AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (somente código gerenciado)</span><span class="sxs-lookup"><span data-stu-id="db6ba-145">[AttachedEditControl Property](/previous-versions/ms582239(v=vs.100)) (managed code only)</span></span>
-   [<span data-ttu-id="db6ba-146">**Propriedade de automostrar**</span><span class="sxs-lookup"><span data-stu-id="db6ba-146">**AutoShow Property**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

<span data-ttu-id="db6ba-147">Essas APIs funcionam em um ambiente de confiança parcial, como uma página da Web, permitindo que você instancie um objeto [**PenInputPanel**](peninputpanel-class.md) , anexe-o a um controle e desabilite o painel de entrada para esse controle.</span><span class="sxs-lookup"><span data-stu-id="db6ba-147">These APIs function in a partial trust environment, such as a Web page, enabling you to instantiate a [**PenInputPanel**](peninputpanel-class.md) object, attach it to a control, and disable Input Panel for that control.</span></span> <span data-ttu-id="db6ba-148">Para obter mais informações, consulte Programando o painel de entrada usando a classe PenInputPanel e a [tinta na Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="db6ba-148">For more information, see Programming the Input Panel Using the PenInputPanel Class and [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="the-peninputpanel-object"></a><span data-ttu-id="db6ba-149">O objeto PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="db6ba-149">The PenInputPanel Object</span></span>

<span data-ttu-id="db6ba-150">O restante deste tópico descreve como usar o objeto [**PenInputPanel**](peninputpanel-class.md) em seus aplicativos habilitados para Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="db6ba-150">The rest of this topic describes how to use the [**PenInputPanel**](peninputpanel-class.md) object in your Tablet PC–enabled applications.</span></span> <span data-ttu-id="db6ba-151">Mais especificamente, este tópico refere-se ao objeto **PenInputPanel** ao discutir o objeto de programação, o painel de entrada da caneta ao se referir ao elemento da interface do usuário e ao painel de entrada do PC (ou painel de entrada) ao se referir ao painel de entrada global normalmente encontrado no lado da tela do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="db6ba-151">More specifically, this topic refers to the **PenInputPanel** object when discussing the programming object, the pen input panel when referring to the UI element, and the PC Input Panel (or Input Panel) when referring to the global input panel typically found on the side of the Tablet PC screen.</span></span>

<span data-ttu-id="db6ba-152">As seções a seguir descrevem o objeto [**PenInputPanel**](peninputpanel-class.md) e a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="db6ba-152">The following sections describe the [**PenInputPanel**](peninputpanel-class.md) object and UI.</span></span>

-   [<span data-ttu-id="db6ba-153">Sobre o painel de entrada</span><span class="sxs-lookup"><span data-stu-id="db6ba-153">About the Input Panel</span></span>](about-the-input-panel.md)
-   [<span data-ttu-id="db6ba-154">Instanciando a classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="db6ba-154">Instantiating the PenInputPanel Class</span></span>](instantiating-the-peninputpanel-class.md)
-   [<span data-ttu-id="db6ba-155">Suporte ao factor</span><span class="sxs-lookup"><span data-stu-id="db6ba-155">Factoid Support</span></span>](factoid-support.md)
-   [<span data-ttu-id="db6ba-156">Estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="db6ba-156">Text Services Framework</span></span>](text-services-framework.md)
-   [<span data-ttu-id="db6ba-157">Práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="db6ba-157">Best Practices</span></span>](best-practices.md)

 

 
