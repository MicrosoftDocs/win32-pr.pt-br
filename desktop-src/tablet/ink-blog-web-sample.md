---
description: O aplicativo de exemplo de blog de tinta demonstra como criar uma classe de UserControl gerenciada que tem capacidade de tinta e hospedar esse controle no Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Exemplo da Web do blog de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090014"
---
# <a name="ink-blog-web-sample"></a><span data-ttu-id="43022-103">Exemplo da Web do blog de tinta</span><span class="sxs-lookup"><span data-stu-id="43022-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="43022-104">O aplicativo de exemplo de blog de tinta demonstra como criar uma classe de [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) gerenciada que tem capacidade de tinta e hospedar esse controle no Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="43022-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="43022-105">O exemplo também demonstra uma técnica para enviar dados de tinta em uma rede usando HTTP e para manter a tinta em um servidor.</span><span class="sxs-lookup"><span data-stu-id="43022-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="43022-106">Você deve ter o Microsoft Serviços de Informações da Internet (IIS) com o ASP.NET instalado para executar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="43022-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="43022-107">Verifique se o computador atende aos requisitos necessários para que os aplicativos ASP.NET sejam executados no computador.</span><span class="sxs-lookup"><span data-stu-id="43022-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="43022-108">Se você executar este exemplo em um computador sem Tablet PC com o Microsoft Windows XP Tablet PC Edition Development Kit 1,7 instalado, o recurso de reconhecimento de texto para o título da tinta não funcionará.</span><span class="sxs-lookup"><span data-stu-id="43022-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="43022-109">Isso ocorre porque um computador não Tablet PC com o SDK do Tablet PC 1,7 instalado não tem reconhecedores.</span><span class="sxs-lookup"><span data-stu-id="43022-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="43022-110">O restante do aplicativo é executado conforme descrito.</span><span class="sxs-lookup"><span data-stu-id="43022-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="43022-111">Visão geral</span><span class="sxs-lookup"><span data-stu-id="43022-111">Overview</span></span>

<span data-ttu-id="43022-112">O exemplo de blog de tinta cria um blog habilitado para tinta.</span><span class="sxs-lookup"><span data-stu-id="43022-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="43022-113">InkBlogWeb é um aplicativo ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="43022-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="43022-114">A entrada de tinta é realizada por meio de um controle de usuário que é referenciado de uma página do ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="43022-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="43022-115">O controle de usuário detecta se os componentes da plataforma Tablet PC estão instalados no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="43022-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="43022-116">Nesse caso, o controle de usuário apresenta o usuário com duas áreas habilitadas para tinta na página da Web: uma para inserir um título para a entrada do blog e outra para o corpo da entrada.</span><span class="sxs-lookup"><span data-stu-id="43022-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="43022-117">Se os componentes da plataforma do Tablet PC não estiverem instalados, o usuário receberá um controle de caixa de texto padrão para o título e corpo da entrada.</span><span class="sxs-lookup"><span data-stu-id="43022-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="43022-118">Quando o usuário termina de criar a entrada, ela clica em um botão, adiciona um blog e a postagem é enviada ao servidor Web para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="43022-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="43022-119">No servidor, o aplicativo salva o texto do título e a data de lançamento, bem como uma referência a um arquivo de Graphics Interchange Format (GIF).</span><span class="sxs-lookup"><span data-stu-id="43022-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="43022-120">O arquivo GIF, também salvo no servidor, contém os dados de tinta do corpo em um arquivo GIF reforçada.</span><span class="sxs-lookup"><span data-stu-id="43022-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="43022-121">Para obter mais informações sobre o formato GIF reforçada, consulte [armazenando tinta em HTML](storing-ink-in-html.md).</span><span class="sxs-lookup"><span data-stu-id="43022-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="43022-122">Há dois projetos na solução InkBlog: o projeto **InkBlogControls** e o projeto **InkBlogWeb** .</span><span class="sxs-lookup"><span data-stu-id="43022-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="43022-123">Projeto InkBlogControls</span><span class="sxs-lookup"><span data-stu-id="43022-123">InkBlogControls Project</span></span>

<span data-ttu-id="43022-124">O projeto **InkBlogControls** é um projeto [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) que contém o código para o controle de usuário que permite a escrita à tinta na página da Web.</span><span class="sxs-lookup"><span data-stu-id="43022-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="43022-125">O código para esse controle, o controle InkArea, está no arquivo InkArea. cs.</span><span class="sxs-lookup"><span data-stu-id="43022-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="43022-126">A `InkArea` classe herda da classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="43022-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="43022-127">O construtor para o `InkArea` controle chama um método auxiliar, `CreateInkCollectionSurface` .</span><span class="sxs-lookup"><span data-stu-id="43022-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



<span data-ttu-id="43022-128">O `CreateInkCollectionSurface` método determina se os componentes de tinta do Tablet PC estão disponíveis no cliente ao tentar criar uma instância da classe [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="43022-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="43022-129">Se a chamada para o `CreateInkCollectionSurface` método for bem sucedido, o método retornará um objeto de [painel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) como o controle.</span><span class="sxs-lookup"><span data-stu-id="43022-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



<span data-ttu-id="43022-130">Se o Construtor falhar porque os arquivos da plataforma de escrita à tinta não são encontrados, o `InputArea` controle é instanciado como um controle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) em vez de um controle [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="43022-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="43022-131">Em seguida, o Construtor dimensiona o controle para o tamanho do controle de usuário pai e o adiciona à coleção de controles do pai.</span><span class="sxs-lookup"><span data-stu-id="43022-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="43022-132">A classe de controle InkArea implementa três propriedades públicas interessantes: InkData, TextData e webhabilited.</span><span class="sxs-lookup"><span data-stu-id="43022-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="43022-133">A propriedade InkData é somente leitura e fornece acesso aos dados de tinta serializados, se o cliente oferecer suporte à entrada de tinta.</span><span class="sxs-lookup"><span data-stu-id="43022-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="43022-134">Se o cliente não oferecer suporte à escrita à tinta, a propriedade InkData obterá uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="43022-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="43022-135">A propriedade InkData chama um método auxiliar, SerializeInkData, para determinar se o cliente dá suporte à escrita à tinta.</span><span class="sxs-lookup"><span data-stu-id="43022-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



<span data-ttu-id="43022-136">No `SerializeInkData` método, a conversão em [InkCollector](/previous-versions/ms583683(v=vs.100)) é necessária ao obter o objeto de [tinta](/previous-versions/ms583670(v=vs.100)) , porque `inputArea` é declarado como um [controle](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="43022-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="43022-137">Se o objeto de tinta contiver traços, os dados de tinta serão salvos na `inkDataBytes` matriz de bytes como um gif (especificado usando o valor de enumeração [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="43022-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="43022-138">Em seguida, o método converte a matriz de bytes em uma cadeia de caracteres codificada em Base64 e retorna essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="43022-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="43022-139">Supondo que o cliente possa executar o reconhecimento, a `TextData` propriedade retorna o objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) de passar os dados de tinta para um reconhecedor de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="43022-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="43022-140">Se o cliente não tiver reconhecimento de tinta, o conteúdo da caixa de texto será retornado, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="43022-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



<span data-ttu-id="43022-141">A `TextData` propriedade chama um método auxiliar, `RecognizeInkData` , mostrado no código a seguir, para executar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="43022-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="43022-142">Quando os mecanismos de reconhecimento estão presentes no sistema, o `RecognizeInkData` método retorna uma cadeia de caracteres contendo a propriedade [TopString](/previous-versions/ms572009(v=vs.100)) do objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="43022-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="43022-143">Caso contrário, ele retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="43022-143">Otherwise, it returns an empty string.</span></span>


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



<span data-ttu-id="43022-144">A `InkEnabled` propriedade é um valor booliano somente leitura que indica se há suporte para a escrita à tinta no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="43022-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="43022-145">Outro membro público importante da `InkArea` classe Control é o `DisposeResources` método.</span><span class="sxs-lookup"><span data-stu-id="43022-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="43022-146">Esse método chama internamente o `Dispose` método para garantir que todos os recursos utilizados pelo controle de usuário sejam limpos.</span><span class="sxs-lookup"><span data-stu-id="43022-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="43022-147">Qualquer aplicativo que usa o `InkArea` controle deve chamar o `DisposeResources` método quando ele for concluído usando o controle.</span><span class="sxs-lookup"><span data-stu-id="43022-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="43022-148">Projeto InkBlogWeb</span><span class="sxs-lookup"><span data-stu-id="43022-148">InkBlogWeb Project</span></span>

<span data-ttu-id="43022-149">O projeto InkBlogWeb é um projeto de implantação de instalação da Web que faz referência ao `InkArea` controle para fornecer a funcionalidade de Blogs.</span><span class="sxs-lookup"><span data-stu-id="43022-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="43022-150">Para obter mais informações sobre projetos de implantação da instalação da Web, consulte [implantação de um projeto de instalação da Web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="43022-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="43022-151">Há dois arquivos. aspx que implementam o exemplo de blog: default. aspx e addblog. aspx.</span><span class="sxs-lookup"><span data-stu-id="43022-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="43022-152">Default. aspx é a página padrão para o aplicativo InkBlogWeb.</span><span class="sxs-lookup"><span data-stu-id="43022-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="43022-153">O arquivo code-behind para esta página é default. aspx. cs.</span><span class="sxs-lookup"><span data-stu-id="43022-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="43022-154">Esta página fornece um link para a página que contém o novo formulário de entrada de blog e exibe as entradas de blog existentes.</span><span class="sxs-lookup"><span data-stu-id="43022-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="43022-155">Esse processo é descrito posteriormente, após o exame a seguir da página novo formulário de entrada de blog, addblog. aspx.</span><span class="sxs-lookup"><span data-stu-id="43022-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="43022-156">Addblog. aspx e seu arquivo code-behind, addblog. aspx. cs, contêm a lógica e o código da interface do usuário para criar novas entradas de blog.</span><span class="sxs-lookup"><span data-stu-id="43022-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="43022-157">AddBlox. aspx faz referência a duas instâncias da classe de controle InkArea criada no projeto InkBlogControls usando o elemento HTML OBJECT, como mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="43022-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="43022-158">Uma instância tem um `id` atributo de inkBlogTitle e a outra tem um atributo de ID de inkBlogBody.</span><span class="sxs-lookup"><span data-stu-id="43022-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="43022-159">O assembly InkBlogControls.dll deve estar presente no mesmo diretório que a página. aspx que faz referência a ele.</span><span class="sxs-lookup"><span data-stu-id="43022-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="43022-160">O projeto de implantação da instalação da Web garante que esse é o caso, conforme evidenciado pela presença do item "saída primária do InkBlogControls" no projeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="43022-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="43022-161">O controle título tem apenas 48 pixels de altura para facilitar a entrada de uma única linha de tinta para o título.</span><span class="sxs-lookup"><span data-stu-id="43022-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="43022-162">O controle corpo tem 296 pixels de altura para liberar espaço para entradas de blog maiores de várias linhas ou talvez desenhos.</span><span class="sxs-lookup"><span data-stu-id="43022-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="43022-163">Os controles InkArea são conectados a uma função de script do lado do cliente, addblog, por meio de um manipulador de eventos onclick do elemento de botão HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="43022-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="43022-164">Há também um formulário HTML na página que contém três elementos de entrada ocultos: BlogTitleText, BlogBodyText e BlogBodyInkData.</span><span class="sxs-lookup"><span data-stu-id="43022-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="43022-165">Esse formulário é usado para postar os dados de entrada do blog de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="43022-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="43022-166">Addblog. aspx é o manipulador de postback definido para o formulário.</span><span class="sxs-lookup"><span data-stu-id="43022-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="43022-167">A função addblog-escrita no Microsoft JScript <entity type="reg"/> – extrai os dados do blog dos controles InkArea e posta os resultados no servidor.</span><span class="sxs-lookup"><span data-stu-id="43022-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



<span data-ttu-id="43022-168">Quando os dados chegam ao servidor, o código em addblog. aspx. cs verifica o manipulador de \_ eventos de carregamento de página para ver se a Propriedade Form do objeto HttpRequest contém quaisquer dados.</span><span class="sxs-lookup"><span data-stu-id="43022-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="43022-169">Nesse caso, ele cria um nome de arquivo com base na hora atual do sistema, coloca os dados do formulário em três variáveis de cadeia de caracteres e grava os dados em um arquivo HTML e um arquivo GIF que contém os dados de tinta, se presente, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="43022-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



<span data-ttu-id="43022-170">Para obter mais detalhes sobre os métodos auxiliares, consulte o código-fonte de exemplo.</span><span class="sxs-lookup"><span data-stu-id="43022-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="43022-171">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="43022-171">Running the Sample</span></span>

<span data-ttu-id="43022-172">O SDK do Tablet PC 1,7 instala o exemplo da Web do blog de tinta por padrão.</span><span class="sxs-lookup"><span data-stu-id="43022-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="43022-173">Para executar o exemplo, no Internet Explorer, navegue até https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx .</span><span class="sxs-lookup"><span data-stu-id="43022-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="43022-174">Se você estiver executando o Windows Server 2003, substitua o nome do computador por "localhost".</span><span class="sxs-lookup"><span data-stu-id="43022-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="43022-175">Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK.</span><span class="sxs-lookup"><span data-stu-id="43022-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="43022-176">Você deve concluir uma instalação personalizada e selecionar a subopção "amostras da Web pré-compiladas" para instalá-las.</span><span class="sxs-lookup"><span data-stu-id="43022-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="43022-177">Você também pode executar o exemplo abrindo e compilando o projeto no Microsoft Visual Studio <entity type="reg"/> .net e, em seguida, implantando-o em um computador separado que executa o IIS.</span><span class="sxs-lookup"><span data-stu-id="43022-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="43022-178">Solucionando problemas do exemplo</span><span class="sxs-lookup"><span data-stu-id="43022-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="43022-179">Três áreas que podem causar dificuldades ao executar ou hospedar o exemplo são permissões e reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="43022-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="43022-180">Permissões</span><span class="sxs-lookup"><span data-stu-id="43022-180">Permissions</span></span>

<span data-ttu-id="43022-181">O exemplo requer permissões de gravação na pasta raiz virtual para a conta que está tentando criar uma nova entrada de blog.</span><span class="sxs-lookup"><span data-stu-id="43022-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="43022-182">Por padrão, a versão compilada do exemplo fornecido no SDK do Tablet PC 1,7 tem as permissões corretas definidas para atender a esse requisito.</span><span class="sxs-lookup"><span data-stu-id="43022-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="43022-183">Se você criar e implantar o exemplo usando o projeto de implantação de instalação da Web fornecido, deverá conceder ao grupo% MACHINENAME% \\ usuários o acesso de gravação para a pasta do sistema de arquivos apontada pela raiz virtual InkBlogWeb (por exemplo, C: \\ Inetpub \\ wwwroot \\ InkBlogWeb).</span><span class="sxs-lookup"><span data-stu-id="43022-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="43022-184">O grupo usuários inclui a conta anônima usada pelo IIS, permitindo assim que o aplicativo ASP.NET grave as novas entradas de blog no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="43022-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="43022-185">Uma alternativa é remover o acesso anônimo à raiz virtual e forçar a autenticação.</span><span class="sxs-lookup"><span data-stu-id="43022-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="43022-186">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="43022-186">Recognition</span></span>

<span data-ttu-id="43022-187">Os reconhecedores de manuscrito devem ser instalados para reconhecer a tinta no título do blog.</span><span class="sxs-lookup"><span data-stu-id="43022-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="43022-188">Se você acessar o aplicativo InkBlog de um computador com um sistema operacional diferente do Windows XP Tablet PC Edition, mas com o SDK 1,7 do Tablet PC instalado, poderá escrever tinta nos controles InkArea, mas os mecanismos de reconhecimento não estarão presentes e nenhum título será exibido para suas entradas de blog.</span><span class="sxs-lookup"><span data-stu-id="43022-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="43022-189">No entanto, o conteúdo de tinta no corpo ainda aparece.</span><span class="sxs-lookup"><span data-stu-id="43022-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="43022-190">Configuração da máquina</span><span class="sxs-lookup"><span data-stu-id="43022-190">Machine Configuration</span></span>

<span data-ttu-id="43022-191">Se você instalou o ASP.NET e o .NET Framework em um computador e, em seguida, desinstala e reinstala o IIS, os mapas de script serão interrompidos e ASP.NET não funcionará.</span><span class="sxs-lookup"><span data-stu-id="43022-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="43022-192">Se isso acontecer, você poderá reparar os mapas de script ASP.NET com a ferramenta de registro do IIS ASP.NET (ASPNET \_regiis.exe-i).</span><span class="sxs-lookup"><span data-stu-id="43022-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43022-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43022-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="43022-194">[Controles InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="43022-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="43022-195">Tinta na Web</span><span class="sxs-lookup"><span data-stu-id="43022-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="43022-196">Formatos de dados de tinta</span><span class="sxs-lookup"><span data-stu-id="43022-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="43022-197">Classe System. Windows. Forms. UserControl</span><span class="sxs-lookup"><span data-stu-id="43022-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
