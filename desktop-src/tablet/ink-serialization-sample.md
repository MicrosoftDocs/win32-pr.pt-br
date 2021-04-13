---
description: Este exemplo demonstra como serializar e desserializar tinta em vários formatos.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Amostra de serialização de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e898f91db17efcb7579c067e7db5c422da8213a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501401"
---
# <a name="ink-serialization-sample"></a><span data-ttu-id="f3da0-103">Amostra de serialização de tinta</span><span class="sxs-lookup"><span data-stu-id="f3da0-103">Ink Serialization Sample</span></span>

<span data-ttu-id="f3da0-104">Este exemplo demonstra como serializar e desserializar tinta em vários formatos.</span><span class="sxs-lookup"><span data-stu-id="f3da0-104">This sample demonstrates how to serialize and de-serialize ink in various formats.</span></span> <span data-ttu-id="f3da0-105">O aplicativo representa um formulário com campos para inserir nome, sobrenome e assinatura.</span><span class="sxs-lookup"><span data-stu-id="f3da0-105">The application represents a form with fields for inputting first name, last name, and signature.</span></span> <span data-ttu-id="f3da0-106">O usuário pode salvar esses dados como ISF (formato serializado de tinta pura), linguagem XML (XML) usando ISF codificado na base64 ou HTML, que faz referência à tinta em uma imagem GIF (Graphics Interchange Format) codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="f3da0-106">The user may save this data as pure ink serialized format (ISF), Extensible Markup Language (XML) using base64 encoded ISF, or HTML, which references ink in a base64 encoded fortified Graphics Interchange Format (GIF) image.</span></span> <span data-ttu-id="f3da0-107">O aplicativo também permite que o usuário abra arquivos que foram salvos como XML e formatos ISF.</span><span class="sxs-lookup"><span data-stu-id="f3da0-107">The application also enables the user to open files that were saved as XML and ISF formats.</span></span> <span data-ttu-id="f3da0-108">O formato ISF usa propriedades estendidas para armazenar o nome e o sobrenome, enquanto os formatos XML e HTML armazenam essas informações em atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="f3da0-108">The ISF format uses extended properties to store the first name and last name, whereas the XML and HTML formats store this information in custom attributes.</span></span>

<span data-ttu-id="f3da0-109">Este exemplo não dá suporte ao carregamento do formato HTML porque o HTML não é adequado para armazenar dados estruturados.</span><span class="sxs-lookup"><span data-stu-id="f3da0-109">This sample does not support loading from the HTML format, because HTML is not suitable for storing structured data.</span></span> <span data-ttu-id="f3da0-110">Como os dados são separados em nome, assinatura e assim por diante, é necessário um formato que preserve essa separação, como XML ou outro tipo de formato de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f3da0-110">Because the data is separated into name, signature, and so on, a format that preserves this separation, such as XML or another kind of database format, is required.</span></span>

<span data-ttu-id="f3da0-111">O HTML é muito útil em um ambiente no qual a formatação é importante, como em um documento de processamento de texto.</span><span class="sxs-lookup"><span data-stu-id="f3da0-111">HTML is very useful in an environment in which formatting is important, such as in a word processing document.</span></span> <span data-ttu-id="f3da0-112">O HTML que é salvo por este exemplo usa GIFs reforçada.</span><span class="sxs-lookup"><span data-stu-id="f3da0-112">The HTML that is saved by this sample uses fortified GIFs.</span></span> <span data-ttu-id="f3da0-113">Esses GIFs têm ISF incorporados neles, o que preserva a fidelidade total da tinta.</span><span class="sxs-lookup"><span data-stu-id="f3da0-113">These GIFs have ISF embedded within them, which preserves the full fidelity of the ink.</span></span> <span data-ttu-id="f3da0-114">Um aplicativo de processamento de texto pode salvar um documento que contém vários tipos de dados, como imagens, tabelas, texto formatado e tinta persistente em um formato HTML.</span><span class="sxs-lookup"><span data-stu-id="f3da0-114">A word processing application can save a document containing multiple types of data, such as images, tables, formatted text, and ink persisted in an HTML format.</span></span> <span data-ttu-id="f3da0-115">Esse HTML seria renderizado em navegadores que não reconhecem tinta.</span><span class="sxs-lookup"><span data-stu-id="f3da0-115">This HTML would render in browsers that do not recognize ink.</span></span> <span data-ttu-id="f3da0-116">No entanto, quando carregado em um aplicativo habilitado para tinta, a fidelidade total da tinta original está disponível e pode ser renderizada, editada ou usada para reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="f3da0-116">However, when loaded into an application that is ink-enabled, the full fidelity of the original ink is available and can be rendered, edited, or used for recognition.</span></span>

<span data-ttu-id="f3da0-117">Os recursos a seguir são usados neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3da0-117">The following features are used in this sample:</span></span>

-   <span data-ttu-id="f3da0-118">O método [Load](/previous-versions/ms569609(v=vs.100)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f3da0-118">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method</span></span>
-   <span data-ttu-id="f3da0-119">O método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f3da0-119">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method</span></span>
-   <span data-ttu-id="f3da0-120">A propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) do objeto de [tinta](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f3da0-120">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property</span></span>

## <a name="collecting-ink"></a><span data-ttu-id="f3da0-121">Coletando tinta</span><span class="sxs-lookup"><span data-stu-id="f3da0-121">Collecting Ink</span></span>

<span data-ttu-id="f3da0-122">Primeiro, faça referência à API do Tablet PC, que é instalada com o SDK (Software Development Kit) do Windows Vista e do Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="f3da0-122">First, reference the Tablet PC API, which are installed with the Windows Vista and Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="f3da0-123">O construtor cria e habilita um [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , para o formulário.</span><span class="sxs-lookup"><span data-stu-id="f3da0-123">The constructor creates and enables an [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic`, for the form.</span></span>


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a><span data-ttu-id="f3da0-124">Salvando um arquivo</span><span class="sxs-lookup"><span data-stu-id="f3da0-124">Saving a File</span></span>

<span data-ttu-id="f3da0-125">O `SaveAsMenu_Click` método manipula a caixa de diálogo Salvar como, cria um fluxo de arquivo no qual salvar os dados de tinta e chama o método salvar que corresponde à opção do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3da0-125">The `SaveAsMenu_Click` method handles the Save As dialog box, creates a file stream in which to save the ink data, and calls the save method that corresponds to the user's choice.</span></span>

## <a name="saving-to-an-isf-file"></a><span data-ttu-id="f3da0-126">Salvando em um arquivo ISF</span><span class="sxs-lookup"><span data-stu-id="f3da0-126">Saving to an ISF File</span></span>

<span data-ttu-id="f3da0-127">No `SaveISF` método, os valores de First e Last Name são adicionados à propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) da propriedade [Ink](/previous-versions/ms836505(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , antes que a tinta seja serializada e gravada no arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3da0-127">In the `SaveISF` method, the first and last name values are added to the [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property of the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [Ink](/previous-versions/ms836505(v=msdn.10)) property, before the ink is serialized and written to the file.</span></span> <span data-ttu-id="f3da0-128">Depois que a tinta for serializada, os valores de nome e sobrenome serão removidos da Propriedade ExtendedProperties do objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3da0-128">After the ink has been serialized, the first and last name values are removed from the [Ink](/previous-versions/aa515768(v=msdn.10)) object's ExtendedProperties property.</span></span>


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a><span data-ttu-id="f3da0-129">Salvando em um arquivo XML</span><span class="sxs-lookup"><span data-stu-id="f3da0-129">Saving to an XML File</span></span>

<span data-ttu-id="f3da0-130">No `SaveXML` método, um objeto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) é usado para criar e gravar em um documento XML.</span><span class="sxs-lookup"><span data-stu-id="f3da0-130">In the `SaveXML` method, an [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) object is used to create and write to an XML document.</span></span> <span data-ttu-id="f3da0-131">Usando o método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) , a tinta é primeiro convertida em uma matriz de bytes de formato serializado de tinta codificada em Base64 e, em seguida, a matriz de bytes é convertida em uma cadeia de caracteres a ser gravada no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="f3da0-131">Using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, the ink is first converted to a base64 encoded Ink Serialized Format byte array, and then the byte array is converted to a string to be written out to the XML file.</span></span> <span data-ttu-id="f3da0-132">Os dados de texto do formulário também são gravados no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="f3da0-132">The text data from the form is also written out to the XML file.</span></span>


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a><span data-ttu-id="f3da0-133">Salvando em um arquivo HTML</span><span class="sxs-lookup"><span data-stu-id="f3da0-133">Saving to an HTML File</span></span>

<span data-ttu-id="f3da0-134">O método SaveHTML usa a caixa delimitadora da coleção [strokess](/previous-versions/ms827799(v=msdn.10)) para testar a presença de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f3da0-134">The SaveHTML method uses the bounding box of the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection to test for the presence of a signature.</span></span> <span data-ttu-id="f3da0-135">Se a assinatura existir, ela será convertida no formato GIF reforçada usando o método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto Ink e gravada em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3da0-135">If the signature exists, it is converted to the fortified GIF format using the ink object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, and written to a file.</span></span> <span data-ttu-id="f3da0-136">Em seguida, o GIF é referenciado no arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="f3da0-136">The GIF is then referenced in the HTML file.</span></span>


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a><span data-ttu-id="f3da0-137">Carregando um arquivo</span><span class="sxs-lookup"><span data-stu-id="f3da0-137">Loading a File</span></span>

<span data-ttu-id="f3da0-138">O `OpenMenu_Click` método manipula a caixa de diálogo abrir, abre o arquivo e chama o método de carregamento que corresponde à escolha do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3da0-138">The `OpenMenu_Click` method handles the Open dialog box, opens the file, and calls the loading method that corresponds to the user's choice.</span></span>

## <a name="loading-an-isf-file"></a><span data-ttu-id="f3da0-139">Carregando um arquivo ISF</span><span class="sxs-lookup"><span data-stu-id="f3da0-139">Loading an ISF File</span></span>

<span data-ttu-id="f3da0-140">O `LoadISF` método lê o arquivo criado anteriormente e converte a matriz de bytes em tinta com o método [Load](/previous-versions/ms569609(v=vs.100)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3da0-140">The `LoadISF` method reads the previously created file and converts the Byte array to ink with the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="f3da0-141">O coletor de tinta está temporariamente desabilitado para atribuir o objeto de tinta a ele.</span><span class="sxs-lookup"><span data-stu-id="f3da0-141">The ink collector is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="f3da0-142">`LoadISF`Em seguida, o método verifica a propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) do objeto Ink para as cadeias de caracteres First e Last Name.</span><span class="sxs-lookup"><span data-stu-id="f3da0-142">The `LoadISF` method then checks the Ink object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property for the first and last name strings.</span></span>


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a><span data-ttu-id="f3da0-143">Carregando um arquivo XML</span><span class="sxs-lookup"><span data-stu-id="f3da0-143">Loading an XML File</span></span>

<span data-ttu-id="f3da0-144">O `LoadXML` método carrega um arquivo XML criado anteriormente, recupera dados do nó de tinta e converte os dados no nó para tinta usando o método [Load](/previous-versions/ms569609(v=vs.100)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3da0-144">The `LoadXML` method loads a previously created XML file, retrieves data from the Ink node, and converts the data in the node to ink using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="f3da0-145">O [InkCollector](/previous-versions/ms836493(v=msdn.10)) está temporariamente desabilitado para atribuir o objeto de tinta a ele.</span><span class="sxs-lookup"><span data-stu-id="f3da0-145">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="f3da0-146">A caixa assinatura é invalidada e as informações de nome e sobrenome são recuperadas do documento XML.</span><span class="sxs-lookup"><span data-stu-id="f3da0-146">The signature box is invalidated, and the first and last name information is retrieved from the XML document.</span></span>


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a><span data-ttu-id="f3da0-147">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="f3da0-147">Closing the Form</span></span>

<span data-ttu-id="f3da0-148">O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3da0-148">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object.</span></span>

 

 
