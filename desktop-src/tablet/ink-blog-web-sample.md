---
description: O aplicativo de exemplo Blog do Ink demonstra como criar uma classe UserControl gerenciada que tenha funcionalidade de inking e hospede esse controle no Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Amostra da Web do blog do Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8796a05861d278015205b5ba0d3775e2e47af6a57ce1fee426c5c0c5011dacd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032354"
---
# <a name="ink-blog-web-sample"></a>Amostra da Web do blog do Ink

O aplicativo de exemplo Blog do Ink demonstra como criar uma classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) gerenciada que tenha funcionalidade de inking e hospede esse controle no Microsoft Internet Explorer. O exemplo também demonstra uma técnica para enviar dados de tinta em uma rede usando HTTP e para persistir tinta em um servidor.

> [!Note]  
> Você deve ter Serviços de Informações da Internet da Microsoft (IIS) com ASP.NET instalado para executar este exemplo. Certifique-se de que seu computador atenda aos requisitos necessários ASP.NET aplicativos para executar em seu computador.

 

> [!Note]  
> Se você executar este exemplo em um computador pc não Tablet com o Microsoft Windows XP Tablet PC Edition Development Kit 1.7 instalado o recurso de reconhecimento de texto para o título de tinta não funcionará. Isso ocorre porque um computador pc não Tablet com o SDK do Tablet PC 1.7 instalado não tem reconhecedores. O restante do aplicativo é desempenho conforme descrito.

 

## <a name="overview"></a>Visão geral

O exemplo de Blog do Ink cria um Weblog habilitado para tinta. InkBlogWeb é um ASP.NET aplicativo. A entrada de tinta é realizada por meio de um controle de usuário referenciado de uma página ASP.NET dados.

O controle de usuário detecta se os componentes da plataforma tablet PC estão instalados no computador cliente. Nesse caso, o controle de usuário apresenta ao usuário duas áreas habilitadas para tinta na página da Web: uma para inking de um título para a entrada do blog e outra para o corpo da entrada. Se os componentes da Plataforma de Tablet PC não estão instalados, o usuário recebe um controle de caixa de texto padrão para o título e o corpo da entrada.

Quando o usuário terminar de criar a entrada, ele clicará em um botão Adicionar Blog e a postagem será enviada ao servidor Web para armazenamento. No servidor, o aplicativo salva o texto do título e a data de postagem, bem como uma referência a um arquivo GRAPHICS INTERCHANGE FORMAT (GIF). O arquivo GIF, também salvo no servidor, contém os dados de tinta do corpo em um arquivo GIF forteizado. Para obter mais informações sobre o formato GIF forteizado, consulte [Armazenamento de tinta em HTML.](storing-ink-in-html.md)

Há dois projetos na solução InkBlog: o **projeto InkBlogControls** e o **projeto InkBlogWeb.**

## <a name="inkblogcontrols-project"></a>InkBlogControls Project

O **projeto InkBlogControls** é um [projeto UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) que contém o código para o controle de usuário que permite a tinta na página da Web. O código para esse controle, o controle InkArea, está no arquivo InkArea.cs.

A `InkArea` Classe herda da [classe UserControl.](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) O construtor do controle `InkArea` chama um método auxiliar, `CreateInkCollectionSurface` .


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



O método determina se os componentes de inking do Tablet PC estão disponíveis no cliente ao tentar criar uma instância da `CreateInkCollectionSurface` [classe InkCollector.](/previous-versions/ms583683(v=vs.100)) Se a chamada para o `CreateInkCollectionSurface` método for bem-sucedida, o método retornará um [objeto Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) como o controle .


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



Se o construtor falhar porque os arquivos da plataforma de tinta não foram encontrados, o controle será instanado como um controle TextBox em vez de um `InputArea` [controle InkCollector.](/previous-versions/ms583683(v=vs.100)) [](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) Em seguida, o construtor tamanhou o controle para o tamanho do controle de usuário pai e o adiciona à coleção Controles pai.

A classe de controle InkArea implementa três propriedades públicas interessantes: InkData, TextData e WebEnabled.

A propriedade InkData é somente leitura e fornece acesso aos dados de tinta serializados, se o cliente dá suporte à tinta. Se o cliente não dá suporte à tinta, a propriedade InkData obtém uma cadeia de caracteres vazia. A propriedade InkData chama um método auxiliar, SerializeInkData, para determinar se o cliente dá suporte à tinta.


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



No método `SerializeInkData` , a cast para [InkCollector](/previous-versions/ms583683(v=vs.100)) é necessária ao obter o objeto [Ink,](/previous-versions/ms583670(v=vs.100)) porque `inputArea` é declarado como um [Controle](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Se o objeto Ink contiver traços, os dados de tinta serão salvos na matriz de byte como um GIF (especificado usando o valor de `inkDataBytes` enumeração [PersistenceFormat).](/previous-versions/ms552503(v=vs.100)) Em seguida, o método converte a matriz de byte em uma cadeia de caracteres codificada em Base64 e retorna essa cadeia de caracteres.

Supondo que o cliente possa executar o reconhecimento, a propriedade retorna o objeto RecognitionResult de passar os dados de tinta `TextData` para um reconhecedor de manuscrito. [](/previous-versions/ms552537(v=vs.100)) Se o cliente não estiver ciente de tinta, o conteúdo da caixa de texto será retornado, conforme mostrado no código a seguir.


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



A `TextData` propriedade chama um método auxiliar, , mostrado no código a `RecognizeInkData` seguir, para realizar o reconhecimento. Quando os mecanismos de reconhecimento estão presentes no sistema, o método retorna uma cadeia de caracteres que contém `RecognizeInkData` a [propriedade TopString](/previous-versions/ms572009(v=vs.100)) do objeto [RecognitionResult.](/previous-versions/ms552537(v=vs.100)) Caso contrário, ele retorna uma cadeia de caracteres vazia.


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



A propriedade é um valor booliana somente leitura que indica se há suporte para a `InkEnabled` inking no computador cliente.

Outro membro público importante da `InkArea` classe de controle é o método `DisposeResources` . Esse método chama internamente o método para garantir que todos os recursos aproveitados pelo `Dispose` controle de usuário sejam limpos. Qualquer aplicativo que usa o `InkArea` controle deve chamar o método quando terminar de usar o controle `DisposeResources` .

## <a name="inkblogweb-project"></a>InkBlogWeb Project

O projeto InkBlogWeb é um projeto de implantação da Instalação da Web que faz referência ao controle para fornecer a `InkArea` funcionalidade de blog. Para obter mais informações sobre projetos de implantação da Instalação da Web, consulte [Implantação de uma instalação da Web Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Há dois arquivos .aspx que implementam o exemplo de blogging: Default.aspx e AddBlog.aspx. Default.aspx é a página padrão para o aplicativo InkBlogWeb. O arquivo code-behind desta página é Default.aspx.cs. Esta página fornece um link para a página que contém o novo formulário de entrada do blog e exibe todas as entradas de blog existentes. Esse processo é descrito posteriormente, após o exame a seguir da nova página de formulário de entrada do blog, AddBlog.aspx.

AddBlog.aspx e seu arquivo code-behind, AddBlog.aspx.cs, contêm a lógica e o código de interface do usuário para criar novas entradas de blog. AddBlox.aspx faz referência a duas instâncias da classe de controle InkArea criadas no projeto InkBlogControls usando o elemento HTML OBJECT, conforme mostrado no exemplo a seguir. Uma instância tem `id` um atributo de inkBlogTitle e a outra tem um atributo de ID de inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

O InkBlogControls.dll assembly deve estar presente no mesmo diretório que a página .aspx que está fazendo referência a ele. O projeto de implantação de Instalação da Web garante que esse seja o caso, conforme evidência da presença do item "Saída primária do InkBlogControls" no Project.

O controle de título tem apenas 48 pixels de altura para facilitar a entrada de uma única linha de tinta para o título. O controle de corpo tem 296 pixels de altura para dar espaço para entradas de blog maiores de várias linhas ou talvez desenhos.

Os controles InkArea estão conectados a uma função de script do lado do cliente, AddBlog, por meio do manipulador de eventos onclick de um elemento HTML BUTTON padrão.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Também há um formulário HTML na página que contém três elementos INPUT ocultos: BlogTitleText, BlogBodyText e BlogBodyInkData. Esse formulário é usado para postar os dados de entrada do blog de volta no servidor. AddBlog.aspx é o manipulador de post-back definido para o formulário.

A função AddBlog escrita no Microsoft JScript extrai os dados do blog dos controles InkArea e posta os <entity type="reg"/> resultados no servidor.


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



Quando os dados chegam ao servidor, o código em AddBlog.aspx.cs verifica o manipulador de eventos Page Load para ver se a propriedade Formulário do objeto \_ HttpRequest contém dados. Nesse caso, ele cria um nome de arquivo com base na hora atual do sistema, coloca os dados do formulário em três variáveis de cadeia de caracteres e grava os dados em um arquivo HTML e um arquivo GIF que contém os dados de tinta, se presentes, conforme mostrado no código a seguir.


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

O SDK do Tablet PC 1.7 instala o exemplo da Web do Blog do Ink por padrão. Para executar o exemplo, em Internet Explorer, navegue até https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Se você estiver executando Windows Server 2003, substitua o nome do computador por "localhost".

> [!Note]  
> Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK. Você deve concluir uma instalação personalizada e selecionar a sub-opção "Exemplos da Web pré-compilados" para instalá-los.

 

Você também pode executar o exemplo abrindo e criando o projeto no Microsoft Visual Studio .NET e, em seguida, implantando-o em um computador separado executando <entity type="reg"/> o IIS.

## <a name="troubleshooting-the-sample"></a>Solucionando problemas do exemplo

Três áreas que podem causar dificuldade ao executar ou hospedar o exemplo são permissões e reconhecimento.

### <a name="permissions"></a>Permissões

O exemplo requer permissões de gravação na pasta raiz virtual para a conta que está tentando criar uma nova entrada de blog. Por padrão, a versão compilada do exemplo fornecida no SDK do Tablet PC 1.7 tem as permissões corretas definidas para atender a esse requisito.

Se você criar e implantar o exemplo usando o projeto de implantação de Instalação da Web fornecido, deverá dar ao grupo %MACHINENAME% Usuários acesso de gravação à pasta do sistema de arquivos apontada pela raiz \\ virtual InkBlogWeb (por exemplo, C: \\ InetPub \\ WWWRoot \\ InkBlogWeb). O grupo Usuários inclui a conta Anônima usada pelo IIS, permitindo que o aplicativo ASP.NET escreva as novas entradas de blog no sistema de arquivos. Uma alternativa é remover o acesso anônimo à raiz virtual e forçar a autenticação.

### <a name="recognition"></a>Reconhecimento

Os reconhecedores de manuscrito devem ser instalados para reconhecer a tinta no título do blog. Se você acessar o aplicativo InkBlog de um computador com um sistema operacional diferente do Windows XP Tablet PC Edition, mas com o SDK do Tablet PC 1.7 instalado, você poderá gravar em tinta nos controles InkArea, mas os mecanismos de reconhecimento não estarão presentes e nenhum título será exibido para suas entradas de blog. No entanto, o conteúdo de tinta no corpo ainda é exibido.

### <a name="machine-configuration"></a>Configuração do computador

Se você tiver instalado o ASP.NET e o .NET Framework em um computador e, em seguida, desinstalar e reinstalar o IIS, os mapas de script serão ASP.NET não funcionarão. Se isso acontecer, você poderá reparar os mapas ASP.NET script com ASP.NET ferramenta de Registro do IIS do ASP.NET (Aspnet \_regiis.exe -i).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inkcollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Tinta na Web](ink-on-the-web.md)
</dt> <dt>

[Formatos de dados de tinta](ink-data-formats.md)
</dt> <dt>

[Sistema. Windows. Classe Forms.UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
