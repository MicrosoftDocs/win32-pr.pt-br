---
description: este tópico aplica-se ao Windows Vista e posterior.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: integração com Windows galeria de fotos e o Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e20b690e2640fb40830721f1c6a3211641d81311724be2c70efae3781171e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549436"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>integração com Windows galeria de fotos e o Windows Explorer

este tópico aplica-se ao Windows Vista e posterior. Ele contém as seções a seguir:

-   [Introdução](#introduction)
-   [integração com o armazenamento de propriedades Windows](#integration-with-the-windows-property-store)
-   [integração com a galeria de fotos Windows](#integration-with-the-windows-photo-gallery)
-   [integração com o Cache de miniaturas Windows](#integration-with-the-windows-thumbnail-cache)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

para habilitar Windows galeria de fotos e Windows Explorer para exibir miniaturas e pesquisar e atualizar metadados de imagem padrão, um codec deve ter uma implementação das interfaces [manipuladordeminiaturai](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associadas a ele. A interface Manipuladordeminiaturai é usada para recuperar miniaturas e preencher o cache de miniaturas, e a interface IPropertyStore é usada para pesquisar e atualizar os metadados associados a um arquivo. a partir do Windows Vista, todos os tipos de arquivo têm miniaturas e metadados, mas tipos de arquivo diferentes exigem implementações diferentes dessas interfaces para recuperar ou gerar as miniaturas e os metadados para eles. O sistema fornece implementações padrão dessas interfaces. a implementação padrão de manipuladordeminiaturai pode ser usada para qualquer formato de imagem habilitado por WIC (Windows Imaging Component). A implementação padrão de IPropertyStore pode ser usada com qualquer formato de imagem habilitado para WIC com base em um formato TIFF ou JPEG. Para associar seu formato de imagem às implementações padrão de ambas as interfaces, você deve adicionar apenas algumas entradas do registro.

as entradas a seguir indicam ao Windows galeria de fotos e ao Windows Explorer que uma extensão de nome de arquivo (. ext) e seu tipo MIME associado estão associados a um formato de imagem.

a entrada a seguir indica Windows e aplicativos que usam o tipo de conteúdo (também conhecido como tipo mime) que um arquivo com uma extensão específica (. ext) é um formato de imagem. O proprietário do tipo de arquivo precisa escolher um `<image sub type value>` que identifique exclusivamente o formato de arquivo e que esse valor de tipo de conteúdo precisa ser registrado no IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

a entrada a seguir indica Windows, Windows pesquisa e aplicativos que usam o [System. Kind](../properties/props-system-kind.md) que uma extensão de nome de arquivo (. ext) deve ser tratada como uma imagem. Especificamente, isso indica que a propriedade System. Kind da extensão do arquivo deve ser definida como Picture.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a>integração com o armazenamento de propriedades Windows

Às vezes, as mesmas propriedades de metadados são expostas em esquemas de metadados diferentes, geralmente com nomes de propriedade diferentes. Quando uma dessas propriedades é atualizada, mas as outras não são, os metadados dentro do arquivo podem ficar fora de sincronia. o manipulador de propriedade de foto fornece a implementação de **IPropertyStore** padrão para imagens e é usado por aplicativos, bem como pela galeria de fotos Windows e Windows Explorer para garantir que todos os metadados em uma imagem permaneçam em sincronia, e que as propriedades exibidas pelos aplicativos sejam consistentes com as exibidas pela galeria de fotos Windows e pelo Windows Explorer. Quando o manipulador de propriedades de foto atualiza metadados, ele garante que essas propriedades sejam atualizadas de forma consistente em todos os formatos de metadados comuns presentes no arquivo.

O manipulador de propriedade de foto deve entender o formato de contêiner e como localizar as várias propriedades dentro dele. Em geral, não é possível que o manipulador de propriedades fotográficas saiba como os vários blocos de metadados são dispostos em um formato de contêiner proprietário. No entanto, se os metadados em seu formato de contêiner forem dispostos da mesma forma que os metadados em um formato de contêiner TIFF ou em um formato de contêiner JPEG, o manipulador de propriedade de foto também poderá aproveitar esse conhecimento para atualizar os metadados de forma consistente em seu formato de contêiner.

Você pode registrar essa associação criando a seguinte entrada de registro. Essa entrada notifica o manipulador de propriedades de foto que o formato de contêiner identificado por esse GUID compreende os mesmos caminhos de linguagem de consulta de metadados que o formato de contêiner com o GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 é o GUID para o formato de contêiner TIFF.)

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

A entrada a seguir associa a implementação padrão do Gerenciador de propriedades de fotos de **IPropertyStore** com arquivos que têm a extensão ". ext". O primeiro GUID é o IID da interface **IPropertyStore** e o segundo é o GUID da implementação do manipulador de propriedades fotográficas dele.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

Os codecs que usam um formato proprietário que não é compatível com o formato de contêiner TIFF ou JPEG devem escrever sua própria implementação **IPropertyStore** .

## <a name="integration-with-the-windows-photo-gallery"></a>integração com a galeria de fotos Windows

Windows A Galeria de fotos é criada no WIC e pode exibir qualquer formato de imagem habilitado para WIC para o qual o codec está instalado. para notificar o sistema de que seu formato de imagem pode ser aberto na galeria de fotos Windows, você precisa criar uma associação de arquivo criando as entradas de registro a seguir.

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

O ProgID normalmente é a extensão de nome de arquivo anexada à palavra "File". (Por exemplo, se a extensão de nome de arquivo for .txt, a ProgID normalmente seria "txtfile".)

Há outras entradas de registro padrão que talvez você precise criar para dar suporte a associações de arquivo; no entanto, como the'y não são específicos do WIC, eles estão além do escopo deste tópico.

## <a name="integration-with-the-windows-thumbnail-cache"></a>integração com o Cache de miniaturas Windows

As duas entradas a seguir indicam que a implementação do provedor de miniaturas do WIC padrão pode ser usada para recuperar miniaturas de arquivos com essa extensão. O primeiro GUID é o IID da interface [manipuladordeminiaturai](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e o segundo é o GUID da implementação do sistema padrão dessa interface. (Todas as entradas em HLCR \\ . ext \\ shellex \\ são repetidas em HKCR \\ SystemFileAssociations \\ . ext \\ shellex \\ .)

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Entradas de registro específicas do codificador](-wic-decoderregentries.md)
</dt> <dt>

[Instalação e registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
