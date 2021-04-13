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
# <a name="ink-serialization-sample"></a>Amostra de serialização de tinta

Este exemplo demonstra como serializar e desserializar tinta em vários formatos. O aplicativo representa um formulário com campos para inserir nome, sobrenome e assinatura. O usuário pode salvar esses dados como ISF (formato serializado de tinta pura), linguagem XML (XML) usando ISF codificado na base64 ou HTML, que faz referência à tinta em uma imagem GIF (Graphics Interchange Format) codificada em base64. O aplicativo também permite que o usuário abra arquivos que foram salvos como XML e formatos ISF. O formato ISF usa propriedades estendidas para armazenar o nome e o sobrenome, enquanto os formatos XML e HTML armazenam essas informações em atributos personalizados.

Este exemplo não dá suporte ao carregamento do formato HTML porque o HTML não é adequado para armazenar dados estruturados. Como os dados são separados em nome, assinatura e assim por diante, é necessário um formato que preserve essa separação, como XML ou outro tipo de formato de banco de dados.

O HTML é muito útil em um ambiente no qual a formatação é importante, como em um documento de processamento de texto. O HTML que é salvo por este exemplo usa GIFs reforçada. Esses GIFs têm ISF incorporados neles, o que preserva a fidelidade total da tinta. Um aplicativo de processamento de texto pode salvar um documento que contém vários tipos de dados, como imagens, tabelas, texto formatado e tinta persistente em um formato HTML. Esse HTML seria renderizado em navegadores que não reconhecem tinta. No entanto, quando carregado em um aplicativo habilitado para tinta, a fidelidade total da tinta original está disponível e pode ser renderizada, editada ou usada para reconhecimento.

Os recursos a seguir são usados neste exemplo:

-   O método [Load](/previous-versions/ms569609(v=vs.100)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10))
-   O método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10))
-   A propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) do objeto de [tinta](/previous-versions/aa515768(v=msdn.10))

## <a name="collecting-ink"></a>Coletando tinta

Primeiro, faça referência à API do Tablet PC, que é instalada com o SDK (Software Development Kit) do Windows Vista e do Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



O construtor cria e habilita um [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , para o formulário.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Salvando um arquivo

O `SaveAsMenu_Click` método manipula a caixa de diálogo Salvar como, cria um fluxo de arquivo no qual salvar os dados de tinta e chama o método salvar que corresponde à opção do usuário.

## <a name="saving-to-an-isf-file"></a>Salvando em um arquivo ISF

No `SaveISF` método, os valores de First e Last Name são adicionados à propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) da propriedade [Ink](/previous-versions/ms836505(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , antes que a tinta seja serializada e gravada no arquivo. Depois que a tinta for serializada, os valores de nome e sobrenome serão removidos da Propriedade ExtendedProperties do objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) .


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



## <a name="saving-to-an-xml-file"></a>Salvando em um arquivo XML

No `SaveXML` método, um objeto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) é usado para criar e gravar em um documento XML. Usando o método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) , a tinta é primeiro convertida em uma matriz de bytes de formato serializado de tinta codificada em Base64 e, em seguida, a matriz de bytes é convertida em uma cadeia de caracteres a ser gravada no arquivo XML. Os dados de texto do formulário também são gravados no arquivo XML.


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



## <a name="saving-to-an-html-file"></a>Salvando em um arquivo HTML

O método SaveHTML usa a caixa delimitadora da coleção [strokess](/previous-versions/ms827799(v=msdn.10)) para testar a presença de uma assinatura. Se a assinatura existir, ela será convertida no formato GIF reforçada usando o método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto Ink e gravada em um arquivo. Em seguida, o GIF é referenciado no arquivo HTML.


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



## <a name="loading-a-file"></a>Carregando um arquivo

O `OpenMenu_Click` método manipula a caixa de diálogo abrir, abre o arquivo e chama o método de carregamento que corresponde à escolha do usuário.

## <a name="loading-an-isf-file"></a>Carregando um arquivo ISF

O `LoadISF` método lê o arquivo criado anteriormente e converte a matriz de bytes em tinta com o método [Load](/previous-versions/ms569609(v=vs.100)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) . O coletor de tinta está temporariamente desabilitado para atribuir o objeto de tinta a ele. `LoadISF`Em seguida, o método verifica a propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) do objeto Ink para as cadeias de caracteres First e Last Name.


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



## <a name="loading-an-xml-file"></a>Carregando um arquivo XML

O `LoadXML` método carrega um arquivo XML criado anteriormente, recupera dados do nó de tinta e converte os dados no nó para tinta usando o método [Load](/previous-versions/ms569609(v=vs.100)) do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) . O [InkCollector](/previous-versions/ms836493(v=msdn.10)) está temporariamente desabilitado para atribuir o objeto de tinta a ele. A caixa assinatura é invalidada e as informações de nome e sobrenome são recuperadas do documento XML.


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



## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) .

 

 
