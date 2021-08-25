---
description: Implementando IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementando IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb32ca6bf5ce0714c06a6f355c319908c6dd3a61b1ac27f6baf13f6285183ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772256"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementando IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>Iwicmetadatablockreader

Vários blocos de metadados geralmente existem em uma imagem, cada um expondo diferentes tipos de informações em formatos diferentes. No modelo Windows WIC (Componente de Imagens), os manipuladores de metadados são componentes distintos que, como decodificadores, podem ser descobertos em tempo de operação. Cada formato de metadados tem um manipulador separado e cada um desses manipuladores de metadados pode ser usado com qualquer formato de imagem que dá suporte ao formato de metadados que ele trata. Portanto, se o formato de imagem for compatível com EXIF, XMP, IPTC ou outro formato, você poderá aproveitar os manipuladores de metadados padrão para esses formatos que acompanham o WIC e você não precisará escrever seus próprios. É claro que, se você criar um novo formato de metadados, deverá escrever um manipulador de metadados para ele, que será descoberto e invocado em tempo de run, assim como os padrões.

> [!Note]  
> Se o formato de imagem for baseado em um contêiner TIFF (Formato de Arquivo de Imagem Marcada) ou JPEG, você não precisará escrever nenhum manipulador de metadados (a menos que você desenvolva um formato de metadados novo ou proprietário). Em contêineres TIFF e JPEG, os blocos de metadados estão localizados em IFDs e cada contêiner tem uma estrutura IFD diferente. O WIC fornece manipuladores IFD para ambos os formatos de contêiner que navegam pela estrutura IFD e delegam aos manipuladores de metadados padrão para acessar os metadados dentro deles. Portanto, se o formato de imagem for baseado em qualquer um desses contêineres, você poderá aproveitar automaticamente os manipuladores IFD do WIC. No entanto, se você tiver um formato de contêiner proprietário que tenha sua própria estrutura de metadados de nível superior exclusiva, deverá escrever um manipulador que possa navegar por essa estrutura de nível superior e delegar aos manipuladores de metadados apropriados, assim como os manipuladores IFD.)

 

Da mesma forma que o WIC fornece uma camada de abstração para aplicativos que permitem que eles trabalhem com todos os formatos de imagem da mesma maneira por meio de um conjunto consistente de interfaces, o WIC fornece uma camada de abstração para autores de codec em relação aos formatos de metadados. Conforme mencionado anteriormente, os autores de codec geralmente não precisam trabalhar diretamente com os vários formatos de metadados que podem estar presentes em uma imagem. No entanto, cada autor de codec é responsável por fornecer uma maneira de enumerar os blocos de metadados para que um manipulador de metadados apropriado possa ser descoberto e instautado para cada bloco.

Você deve implementar essa interface em sua classe de decodificação no nível do quadro. Talvez você também precise implementá-lo na classe de decodificador no nível do contêiner se o formato de imagem expor metadados globais fora de qualquer quadro de imagem individual.

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

-   [Getcontainerformat](#getcontainerformat)
-   [GetCount](#getcount)
-   [Getenumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>Getcontainerformat

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) é o mesmo que o [método GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) em [Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) retorna o número de blocos de metadados de nível superior associados ao quadro.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator retorna**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) um enumerador que o chamador pode usar para enumerar sobre os blocos de metadados no quadro e ler seus metadados. Para implementar esse método, você precisa criar um leitor de metadados para cada bloco de metadados e implementar um objeto de enumeração que enumera na coleção de leitores de metadados. O objeto de enumeração deve implementar [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) para que você possa castiá-lo em IEnumUnknown quando você o retornar no *parâmetro ppIEnumMetadata.*

Ao implementar o objeto de enumeração, você pode criar todos os leitores de metadados ao criar pela primeira vez o objeto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) ou ao criar pela primeira vez o objeto de enumeração, ou pode criar-os de forma mais simples dentro da implementação do método [IEnumUnknown::Next.](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) Em muitos casos, é mais eficiente crie-os de forma mais simples, mas, no exemplo a seguir, todos os leitores de bloco são criados no construtor para economizar espaço.


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



Para criar os leitores de metadados, use o [**método CreateMetadataReaderFromContainer.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) Ao invocar esse método, você passa o GUID do formato de contêiner no *parâmetro guidContainerFormat.* Se você tiver uma preferência de fornecedor para um leitor de metadados, poderá passar o GUID de seu fornecedor preferencial no *parâmetro pGuidVendor.* Por exemplo, se sua empresa grava manipuladores de metadados e você deseja usar seus próprios, se presente, você pode passar o GUID do fornecedor. Na maioria dos casos, basta passar **NULL** e permitir que o sistema selecione o leitor de metadados apropriado. Se você solicitar um fornecedor específico e esse fornecedor tiver um leitor de metadados instalado no computador, o WIC retornará o leitor desse fornecedor. No entanto, se o fornecedor solicitado não tiver um leitor de metadados instalado no computador e se houver um leitor de metadados apropriado disponível, esse leitor será retornado mesmo que não seja do fornecedor preferencial. Se não houver nenhum leitor de metadados no computador para o tipo de metadados no bloco, o fábrica de componentes retornará o Manipulador de Metadados Desconhecidos, que tratará o bloco de metadados como um BLOB (objeto binário grande) e desserializará o bloco de metadados do arquivo sem qualquer tentativa de análise.

Para o *parâmetro dwOptions,* execute uma operação OR entre as [**WICPersistOptions apropriadas**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) com [**o WICMetadataCreationOptions apropriado.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) As **WICPersistOptions descrevem** como o contêiner é colocado. Little-endian é o padrão.

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

O [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) especifica se você deseja obter de volta o UnknownMetadataHandler se nenhum leitor de metadados for encontrado no computador que possa ler o formato de metadados de um bloco específico. **WICMetadataCreationAllowUnknown** é o padrão e você sempre deve permitir a criação do UnknownMetadtataHandler. O UnknownMetadataHandler trata metadados não reconhecedos como um BLOB. Ele não pode analisar, mas grava-o no fluxo como um BLOB e o mantém intacto quando é gravado de volta no fluxo durante a codificação. Isso torna seguro criar manipuladores de metadados para formatos de metadados ou metadados proprietários que não são fornecidas com o sistema. Como os metadados são preservados intactos, mesmo que nenhum manipulador esteja presente no computador que os reconheça, quando um manipulador de metadados apropriado for instalado posteriormente, os metadados ainda estarão lá e poderão ser lidos. Se você não permitir a criação do UnknownMetadataHandler, a alternativa será descartar ou sobrescrever metadados não confirmados. Essa é uma forma de perda de dados.

> [!Note]  
> Se você escrever seu próprio manipulador de metadados para metadados proprietários, nunca deverá incluir referências a nada fora do próprio bloco de metadados. Embora UnknownMetadataHandler preserve os metadados intactos, os metadados são movidos quando os arquivos são editados e as referências a qualquer coisa fora de seu próprio bloco não serão mais válidas quando isso acontecer.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

O *parâmetro pIStream* é o fluxo real que você está decodificando. Antes de passar o fluxo, você deve buscar o início do bloco de metadados para o qual você está solicitando um leitor. O leitor de metadados apropriado para o bloco de metadados na posição atual [no IStream](/windows/desktop/api/objidl/nn-objidl-istream) será retornado no *parâmetro ppiReader.*

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) retorna o leitor de metadados no índice solicitado na coleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**Iwicmetadatablockreader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementando IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
