---
description: Este exemplo demonstra como serializar e des serializar tinta em vários formatos.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Exemplo de serialização de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e71eed5c91bf4fa1524cc52af163516ced0c7362d0d20b8ecf52ac1a08ccd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032264"
---
# <a name="ink-serialization-sample"></a>Exemplo de serialização de tinta

Este exemplo demonstra como serializar e des serializar tinta em vários formatos. O aplicativo representa um formulário com campos para inserir o nome, o sobrenome e a assinatura. O usuário pode salvar esses dados como ISF (formato serializado de tinta pura), linguagem XML (XML) usando ISF codificado em base64 ou HTML, que faz referência à tinta em uma imagem GIF (Graphics Interchange Format) codificada em base64. O aplicativo também permite que o usuário abra arquivos que foram salvos como formatos XML e ISF. O formato ISF usa propriedades estendidas para armazenar o nome e sobrenome, enquanto os formatos XML e HTML armazenam essas informações em atributos personalizados.

Este exemplo não dá suporte ao carregamento do formato HTML, pois o HTML não é adequado para armazenar dados estruturados. Como os dados são separados em nome, assinatura e assim por diante, um formato que preserva essa separação, como XML ou outro tipo de formato de banco de dados, é necessário.

HTML é muito útil em um ambiente no qual a formatação é importante, como em um documento de processamento de palavras. O HTML salvo por este exemplo usa GIFs forteizados. Esses GIFs têm ISF inserido neles, o que preserva a fidelidade total da tinta. Um aplicativo de processamento de palavras pode salvar um documento que contém vários tipos de dados, como imagens, tabelas, texto formatado e tinta persistentes em um formato HTML. Esse HTML renderizaria em navegadores que não reconhecem tinta. No entanto, quando carregado em um aplicativo habilitado para tinta, a fidelidade total da tinta original está disponível e pode ser renderizada, editada ou usada para reconhecimento.

Os seguintes recursos são usados neste exemplo:

-   O [método Load](/previous-versions/aa515768(v=msdn.10)) do [objeto](/previous-versions/ms569609(v=vs.100)) Ink
-   O [método Save](/previous-versions/aa515768(v=msdn.10)) do [objeto](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) Ink
-   A [propriedade](/previous-versions/aa515768(v=msdn.10)) [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) do objeto Ink

## <a name="collecting-ink"></a>Coletando tinta

Primeiro, consulte a API do Tablet PC, que é instalada com o SDK (Software Development Kit) do Windows Vista e Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



O construtor cria e habilita um [InkCollector](/previous-versions/ms836493(v=msdn.10)) `ic` , , para o formulário.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Salvando um arquivo

O método trata a caixa de diálogo Salvar como, cria um fluxo de arquivos no qual salvar os dados de tinta e chama o método save que corresponde à escolha `SaveAsMenu_Click` do usuário.

## <a name="saving-to-an-isf-file"></a>Salvando em um arquivo ISF

No método , os valores de nome e sobrenome são adicionados à propriedade `SaveISF` [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) da propriedade Ink do objeto [InkCollector,](/previous-versions/ms836493(v=msdn.10)) antes que a tinta seja serializada e gravado no arquivo. [](/previous-versions/ms836505(v=msdn.10)) Depois que a tinta for serializada, os valores [](/previous-versions/aa515768(v=msdn.10)) de nome e sobrenome serão removidos da propriedade ExtendedProperties do objeto Ink.


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

No método `SaveXML` , um objeto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) é usado para criar e gravar em um documento XML. Usando o método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [Ink,](/previous-versions/aa515768(v=msdn.10)) a tinta é convertida primeiro em uma matriz de byte formato ISF codificada em base64 e, em seguida, a matriz de byte é convertida em uma cadeia de caracteres a ser escrita no arquivo XML. Os dados de texto do formulário também são gravados no arquivo XML.


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

O método SaveHTML usa a caixa delimitada da coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) para testar a presença de uma assinatura. Se a assinatura existir, ela será convertida no formato GIF com base no método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto de tinta e gravado em um arquivo. O GIF é referenciado no arquivo HTML.


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

O método trata a caixa de diálogo Abrir, abre o arquivo e chama o método de carregamento que corresponde à `OpenMenu_Click` escolha do usuário.

## <a name="loading-an-isf-file"></a>Carregando um arquivo ISF

O método lê o arquivo criado anteriormente e converte a matriz byte em tinta com o método Load do `LoadISF` [objeto Ink.](/previous-versions/ms569609(v=vs.100)) [](/previous-versions/aa515768(v=msdn.10)) O coletor de tinta está temporariamente desabilitado para atribuir o objeto Ink a ele. Em `LoadISF` seguida, o método verifica a propriedade [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) do objeto Ink para as cadeias de caracteres de nome e sobrenome.


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

O método carrega um arquivo XML criado anteriormente, recupera dados do nó Ink e converte os dados no nó em tinta usando o método Load do `LoadXML` [objeto Ink.](/previous-versions/ms569609(v=vs.100)) [](/previous-versions/aa515768(v=msdn.10)) O [InkCollector está](/previous-versions/ms836493(v=msdn.10)) temporariamente desabilitado para atribuir o objeto Ink a ele. A caixa de assinatura é invalidada e as informações de nome e sobrenome são recuperadas do documento XML.


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

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o [objeto InkCollector.](/previous-versions/ms836493(v=msdn.10))

 

 
