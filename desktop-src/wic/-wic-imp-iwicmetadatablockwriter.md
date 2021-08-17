---
description: Implementando IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementando IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d49912ece0cc1e3c2299ace0a15f112ef7ab65ac03863b855b8a9ee64e62e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964965"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementando IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

A classe de codificação no nível do quadro implementa essa interface para expor todos os blocos de metadados e solicitar o autor de metadados apropriado para cada bloco. Se o formato de imagem for compatível com metadados globais, fora de qualquer quadro individual, você também deverá implementar essa interface na classe do codificador no nível do contêiner. Para obter uma discussão mais detalhada sobre manipuladores de metadados, consulte a seção [**sobre IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) na seção sobre Como implementar um decodificador WIC-Enabled dados.

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>InitializeFromBlockReader

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa [**um IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) para inicializar o bloqueador. Você pode obter **o IWICMetadataBlockReader** do decodificador que decodificou a imagem.


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



Como inicializar [**o IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) com [**um IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instanam um autor de metadados para cada leitor de metadados exposto pelo objeto **IWICMetadataBlockReader,** o aplicativo não precisa solicitar explicitamente um autor para cada bloco de metadados.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) retorna o objeto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) para o nº bloco de metadados, em que n é o valor passado no *parâmetro nIndex.* Se não houver nenhum autor de metadados registrado que possa manipular o tipo de metadados no nº bloco, a fábrica de componentes retornará o Manipulador de Metadados Desconhecidos, que tratará o bloco de metadados como um BLOB (objeto binário grande). Ele o serializará como um fluxo de bits sem tentar analisar.

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permite que um chamador adicione um novo autor de metadados. Isso será necessário se um aplicativo quiser adicionar metadados de um formato diferente de qualquer um dos blocos de metadados existentes. Por exemplo, um aplicativo pode querer adicionar alguns metadados XMP. Se não houver nenhum bloco de metadados XMP existente, o aplicativo deverá inciar um autor de metadados XMP e usar o **método AddWriter** para incluí-lo na coleção de autores de metadados.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) é usado para adicionar um autor de metadados a um índice específico na coleção. Se um autor de metadados existir no momento nesse índice, o novo deverá substituí-lo.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) é usado para remover um autor de metadados da coleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Instalação e registro do CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



