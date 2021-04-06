---
description: Implementando o IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementando o IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828604"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementando o IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

Vários blocos de metadados geralmente existem em uma imagem, cada um expondo diferentes tipos de informações em formatos diferentes. No modelo do Windows Imaging Component (WIC), os manipuladores de metadados são componentes distintos que, como decodificadores, são detectáveis em tempo de execução. Cada formato de metadados tem um manipulador separado, e cada um desses manipuladores de metadados pode ser usado com qualquer formato de imagem que ofereça suporte ao formato de metadados que ele manipula. Portanto, se o formato de imagem oferecer suporte a EXIF, XMP, IPTC ou outro formato, você poderá aproveitar os manipuladores de metadados padrão para esses formatos fornecidos com o WIC e não precisará escrever o seu próprio. É claro que, se você criar um novo formato de metadados, deverá gravar um manipulador de metadados para ele, que será descoberto e invocado em tempo de execução, assim como os padrões.

> [!Note]  
> Se o formato de imagem for baseado em um formato TIFF ou JPEG, você não precisará escrever manipuladores de metadados (a menos que você desenvolva um formato de metadados novo ou proprietário). Em contêineres TIFF e JPEG, blocos de metadados estão localizados em IFDs, e cada contêiner tem uma estrutura IFD diferente. O WIC fornece manipuladores de IFD para ambos os formatos de contêiner que navegam na estrutura IFD e delegam aos manipuladores de metadados padrão para acessar os metadados dentro deles. Portanto, se o formato da imagem for baseado em qualquer um desses contêineres, você poderá aproveitar automaticamente os manipuladores de IFD do WIC. No entanto, se você tiver um formato de contêiner proprietário que tenha sua própria estrutura de metadados de nível superior exclusiva, deverá escrever um manipulador que possa navegar pela estrutura de nível superior e delegar para os manipuladores de metadados apropriados, assim como os manipuladores de IFD.)

 

Da mesma forma que o WIC fornece uma camada de abstração para aplicativos que permite trabalhar com todos os formatos de imagem da mesma maneira por meio de um conjunto consistente de interfaces, o WIC fornece uma camada de abstração para autores de codec em relação aos formatos de metadados. Conforme observado anteriormente, os autores de codec geralmente não precisam trabalhar diretamente com os vários formatos de metadados que podem estar presentes em uma imagem. No entanto, cada autor de codec é responsável por fornecer uma maneira de enumerar os blocos de metadados para que um manipulador de metadados apropriado possa ser descoberto e instanciado para cada bloco.

Você deve implementar essa interface em sua classe de decodificação de nível de quadro. Talvez você também precise implementá-lo em sua classe de decodificador de nível de contêiner se seu formato de imagem expõe metadados globais fora de qualquer quadro de imagem individual.

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [GetContainerFormat](#getcontainerformat)
-   [GetCount](#getcount)
-   [GetEnumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) é o mesmo que o método [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) na [implementação de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) retorna o número de blocos de metadados de nível superior associados ao quadro.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) retorna um enumerador que o chamador pode usar para enumerar os blocos de metadados no quadro e ler seus metadados. Para implementar esse método, você precisa criar um leitor de metadados para cada bloco de metadados e implementar um objeto de enumeração que enumere sobre a coleção de leitores de metadados. O objeto de enumeração deve implementar [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) para que você possa convertê-lo em IEnumUnknown ao retorná-lo no parâmetro *ppIEnumMetadata* .

Ao implementar o objeto de enumeração, você pode criar todos os leitores de metadados ao criar primeiro o objeto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) ou ao criar o objeto de enumeração pela primeira vez ou pode criá-los lentamente dentro da implementação do método [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) . Em muitos casos, é mais eficiente criá-los lentamente, mas, no exemplo a seguir, os leitores de bloco são todos criados no construtor para economizar espaço.


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



Para criar os leitores de metadados, use o método [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) . Ao invocar esse método, você passa o GUID do formato de contêiner no parâmetro *guidContainerFormat* . Se você tiver uma preferência de fornecedor para um leitor de metadados, poderá passar o GUID do seu fornecedor preferido no parâmetro *pguidVendor* . Por exemplo, se sua empresa escreve manipuladores de metadados e você deseja usar seu próprio, se estiver presente, você pode passar o GUID do fornecedor. Na maioria dos casos, basta passar **NULL** e deixar o sistema selecionar o leitor de metadados apropriado. Se você solicitar um fornecedor específico e esse fornecedor tiver um leitor de metadados instalado no computador, o WIC retornará o leitor desse fornecedor. No entanto, se o fornecedor solicitado não tiver um leitor de metadados instalado no computador e se houver um leitor de metadados apropriado disponível, esse leitor será retornado mesmo que não seja do fornecedor preferido. Se não houver nenhum leitor de metadados no computador para o tipo de metadados no bloco, a fábrica de componentes retornará o manipulador de metadados desconhecido, que tratará o bloco de metadados como um BLOB (objeto binário grande) e desserializará o bloco de metadados do arquivo sem nenhuma tentativa de analisá-lo.

Para o parâmetro *dwOptions* , execute uma operação or entre o [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) apropriado com o [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)apropriado. O **WICPersistOptions** descreve como seu contêiner é apresentado. Little-endian é o padrão.

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

O [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) especifica se você deseja recuperar o UnknownMetadataHandler se nenhum leitor de metadados for encontrado no computador que possa ler o formato de metadados de um bloco específico. **WICMetadataCreationAllowUnknown** é o padrão e você sempre deve permitir a criação do UnknownMetadtataHandler. O UnknownMetadataHandler trata os metadados não reconhecidos como um BLOB. Ele não pode analisá-lo, mas o grava no fluxo como um BLOB e o mantém intacto quando é gravado no fluxo durante a codificação. Isso torna seguro criar manipuladores de metadados para metadados proprietários ou formatos de metadados que não são fornecidos com o sistema. Como os metadados são preservados intactos, mesmo se nenhum manipulador estiver presente no computador que o reconhece, quando um manipulador de metadados apropriado for instalado posteriormente, os metadados ainda estarão lá e poderão ser lidos. Se você não permitir a criação do UnknownMetadataHandler, a alternativa será descartar ou substituir os metadados não reconhecidos. Essa é uma forma de perda de dados.

> [!Note]  
> Se você escrever seu próprio manipulador de metadados para metadados proprietários, nunca deverá incluir referências a nada fora do próprio bloco de metadados. Embora o UnknownMetadataHandler preserve os metadados intactos, os metadados são movidos quando os arquivos são editados, e todas as referências a qualquer coisa fora de seu próprio bloco não serão mais válidas quando isso acontecer.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

O parâmetro *pIStream* é o fluxo real que você está decodificando. Antes de passar no fluxo, você deve procurar o início do bloco de metadados para o qual você está solicitando um leitor. O leitor de metadados apropriado para o bloco de metadados na posição atual em [IStream](/windows/desktop/api/objidl/nn-objidl-istream) será retornado no parâmetro *ppiReader* .

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) retorna o leitor de metadados no índice solicitado na coleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementando IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
