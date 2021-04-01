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
# <a name="ink-blog-web-sample"></a>Exemplo da Web do blog de tinta

O aplicativo de exemplo de blog de tinta demonstra como criar uma classe de [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) gerenciada que tem capacidade de tinta e hospedar esse controle no Microsoft Internet Explorer. O exemplo também demonstra uma técnica para enviar dados de tinta em uma rede usando HTTP e para manter a tinta em um servidor.

> [!Note]  
> Você deve ter o Microsoft Serviços de Informações da Internet (IIS) com o ASP.NET instalado para executar este exemplo. Verifique se o computador atende aos requisitos necessários para que os aplicativos ASP.NET sejam executados no computador.

 

> [!Note]  
> Se você executar este exemplo em um computador sem Tablet PC com o Microsoft Windows XP Tablet PC Edition Development Kit 1,7 instalado, o recurso de reconhecimento de texto para o título da tinta não funcionará. Isso ocorre porque um computador não Tablet PC com o SDK do Tablet PC 1,7 instalado não tem reconhecedores. O restante do aplicativo é executado conforme descrito.

 

## <a name="overview"></a>Visão geral

O exemplo de blog de tinta cria um blog habilitado para tinta. InkBlogWeb é um aplicativo ASP.NET. A entrada de tinta é realizada por meio de um controle de usuário que é referenciado de uma página do ASP.NET.

O controle de usuário detecta se os componentes da plataforma Tablet PC estão instalados no computador cliente. Nesse caso, o controle de usuário apresenta o usuário com duas áreas habilitadas para tinta na página da Web: uma para inserir um título para a entrada do blog e outra para o corpo da entrada. Se os componentes da plataforma do Tablet PC não estiverem instalados, o usuário receberá um controle de caixa de texto padrão para o título e corpo da entrada.

Quando o usuário termina de criar a entrada, ela clica em um botão, adiciona um blog e a postagem é enviada ao servidor Web para armazenamento. No servidor, o aplicativo salva o texto do título e a data de lançamento, bem como uma referência a um arquivo de Graphics Interchange Format (GIF). O arquivo GIF, também salvo no servidor, contém os dados de tinta do corpo em um arquivo GIF reforçada. Para obter mais informações sobre o formato GIF reforçada, consulte [armazenando tinta em HTML](storing-ink-in-html.md).

Há dois projetos na solução InkBlog: o projeto **InkBlogControls** e o projeto **InkBlogWeb** .

## <a name="inkblogcontrols-project"></a>Projeto InkBlogControls

O projeto **InkBlogControls** é um projeto [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) que contém o código para o controle de usuário que permite a escrita à tinta na página da Web. O código para esse controle, o controle InkArea, está no arquivo InkArea. cs.

A `InkArea` classe herda da classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) . O construtor para o `InkArea` controle chama um método auxiliar, `CreateInkCollectionSurface` .


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



O `CreateInkCollectionSurface` método determina se os componentes de tinta do Tablet PC estão disponíveis no cliente ao tentar criar uma instância da classe [InkCollector](/previous-versions/ms583683(v=vs.100)) . Se a chamada para o `CreateInkCollectionSurface` método for bem sucedido, o método retornará um objeto de [painel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) como o controle.


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



Se o Construtor falhar porque os arquivos da plataforma de escrita à tinta não são encontrados, o `InputArea` controle é instanciado como um controle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) em vez de um controle [InkCollector](/previous-versions/ms583683(v=vs.100)) . Em seguida, o Construtor dimensiona o controle para o tamanho do controle de usuário pai e o adiciona à coleção de controles do pai.

A classe de controle InkArea implementa três propriedades públicas interessantes: InkData, TextData e webhabilited.

A propriedade InkData é somente leitura e fornece acesso aos dados de tinta serializados, se o cliente oferecer suporte à entrada de tinta. Se o cliente não oferecer suporte à escrita à tinta, a propriedade InkData obterá uma cadeia de caracteres vazia. A propriedade InkData chama um método auxiliar, SerializeInkData, para determinar se o cliente dá suporte à escrita à tinta.


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



No `SerializeInkData` método, a conversão em [InkCollector](/previous-versions/ms583683(v=vs.100)) é necessária ao obter o objeto de [tinta](/previous-versions/ms583670(v=vs.100)) , porque `inputArea` é declarado como um [controle](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Se o objeto de tinta contiver traços, os dados de tinta serão salvos na `inkDataBytes` matriz de bytes como um gif (especificado usando o valor de enumeração [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ). Em seguida, o método converte a matriz de bytes em uma cadeia de caracteres codificada em Base64 e retorna essa cadeia de caracteres.

Supondo que o cliente possa executar o reconhecimento, a `TextData` propriedade retorna o objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) de passar os dados de tinta para um reconhecedor de manuscrito. Se o cliente não tiver reconhecimento de tinta, o conteúdo da caixa de texto será retornado, conforme mostrado no código a seguir.


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



A `TextData` propriedade chama um método auxiliar, `RecognizeInkData` , mostrado no código a seguir, para executar o reconhecimento. Quando os mecanismos de reconhecimento estão presentes no sistema, o `RecognizeInkData` método retorna uma cadeia de caracteres contendo a propriedade [TopString](/previous-versions/ms572009(v=vs.100)) do objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) . Caso contrário, ele retorna uma cadeia de caracteres vazia.


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



A `InkEnabled` propriedade é um valor booliano somente leitura que indica se há suporte para a escrita à tinta no computador cliente.

Outro membro público importante da `InkArea` classe Control é o `DisposeResources` método. Esse método chama internamente o `Dispose` método para garantir que todos os recursos utilizados pelo controle de usuário sejam limpos. Qualquer aplicativo que usa o `InkArea` controle deve chamar o `DisposeResources` método quando ele for concluído usando o controle.

## <a name="inkblogweb-project"></a>Projeto InkBlogWeb

O projeto InkBlogWeb é um projeto de implantação de instalação da Web que faz referência ao `InkArea` controle para fornecer a funcionalidade de Blogs. Para obter mais informações sobre projetos de implantação da instalação da Web, consulte [implantação de um projeto de instalação da Web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Há dois arquivos. aspx que implementam o exemplo de blog: default. aspx e addblog. aspx. Default. aspx é a página padrão para o aplicativo InkBlogWeb. O arquivo code-behind para esta página é default. aspx. cs. Esta página fornece um link para a página que contém o novo formulário de entrada de blog e exibe as entradas de blog existentes. Esse processo é descrito posteriormente, após o exame a seguir da página novo formulário de entrada de blog, addblog. aspx.

Addblog. aspx e seu arquivo code-behind, addblog. aspx. cs, contêm a lógica e o código da interface do usuário para criar novas entradas de blog. AddBlox. aspx faz referência a duas instâncias da classe de controle InkArea criada no projeto InkBlogControls usando o elemento HTML OBJECT, como mostrado no exemplo a seguir. Uma instância tem um `id` atributo de inkBlogTitle e a outra tem um atributo de ID de inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

O assembly InkBlogControls.dll deve estar presente no mesmo diretório que a página. aspx que faz referência a ele. O projeto de implantação da instalação da Web garante que esse é o caso, conforme evidenciado pela presença do item "saída primária do InkBlogControls" no projeto de implantação.

O controle título tem apenas 48 pixels de altura para facilitar a entrada de uma única linha de tinta para o título. O controle corpo tem 296 pixels de altura para liberar espaço para entradas de blog maiores de várias linhas ou talvez desenhos.

Os controles InkArea são conectados a uma função de script do lado do cliente, addblog, por meio de um manipulador de eventos onclick do elemento de botão HTML padrão.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Há também um formulário HTML na página que contém três elementos de entrada ocultos: BlogTitleText, BlogBodyText e BlogBodyInkData. Esse formulário é usado para postar os dados de entrada do blog de volta para o servidor. Addblog. aspx é o manipulador de postback definido para o formulário.

A função addblog-escrita no Microsoft JScript <entity type="reg"/> – extrai os dados do blog dos controles InkArea e posta os resultados no servidor.


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



Quando os dados chegam ao servidor, o código em addblog. aspx. cs verifica o manipulador de \_ eventos de carregamento de página para ver se a Propriedade Form do objeto HttpRequest contém quaisquer dados. Nesse caso, ele cria um nome de arquivo com base na hora atual do sistema, coloca os dados do formulário em três variáveis de cadeia de caracteres e grava os dados em um arquivo HTML e um arquivo GIF que contém os dados de tinta, se presente, conforme mostrado no código a seguir.


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



Para obter mais detalhes sobre os métodos auxiliares, consulte o código-fonte de exemplo.

## <a name="running-the-sample"></a>Executando o exemplo

O SDK do Tablet PC 1,7 instala o exemplo da Web do blog de tinta por padrão. Para executar o exemplo, no Internet Explorer, navegue até https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Se você estiver executando o Windows Server 2003, substitua o nome do computador por "localhost".

> [!Note]  
> Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK. Você deve concluir uma instalação personalizada e selecionar a subopção "amostras da Web pré-compiladas" para instalá-las.

 

Você também pode executar o exemplo abrindo e compilando o projeto no Microsoft Visual Studio <entity type="reg"/> .net e, em seguida, implantando-o em um computador separado que executa o IIS.

## <a name="troubleshooting-the-sample"></a>Solucionando problemas do exemplo

Três áreas que podem causar dificuldades ao executar ou hospedar o exemplo são permissões e reconhecimento.

### <a name="permissions"></a>Permissões

O exemplo requer permissões de gravação na pasta raiz virtual para a conta que está tentando criar uma nova entrada de blog. Por padrão, a versão compilada do exemplo fornecido no SDK do Tablet PC 1,7 tem as permissões corretas definidas para atender a esse requisito.

Se você criar e implantar o exemplo usando o projeto de implantação de instalação da Web fornecido, deverá conceder ao grupo% MACHINENAME% \\ usuários o acesso de gravação para a pasta do sistema de arquivos apontada pela raiz virtual InkBlogWeb (por exemplo, C: \\ Inetpub \\ wwwroot \\ InkBlogWeb). O grupo usuários inclui a conta anônima usada pelo IIS, permitindo assim que o aplicativo ASP.NET grave as novas entradas de blog no sistema de arquivos. Uma alternativa é remover o acesso anônimo à raiz virtual e forçar a autenticação.

### <a name="recognition"></a>Reconhecimento

Os reconhecedores de manuscrito devem ser instalados para reconhecer a tinta no título do blog. Se você acessar o aplicativo InkBlog de um computador com um sistema operacional diferente do Windows XP Tablet PC Edition, mas com o SDK 1,7 do Tablet PC instalado, poderá escrever tinta nos controles InkArea, mas os mecanismos de reconhecimento não estarão presentes e nenhum título será exibido para suas entradas de blog. No entanto, o conteúdo de tinta no corpo ainda aparece.

### <a name="machine-configuration"></a>Configuração da máquina

Se você instalou o ASP.NET e o .NET Framework em um computador e, em seguida, desinstala e reinstala o IIS, os mapas de script serão interrompidos e ASP.NET não funcionará. Se isso acontecer, você poderá reparar os mapas de script ASP.NET com a ferramenta de registro do IIS ASP.NET (ASPNET \_regiis.exe-i).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Tinta na Web](ink-on-the-web.md)
</dt> <dt>

[Formatos de dados de tinta](ink-data-formats.md)
</dt> <dt>

[Classe System. Windows. Forms. UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
