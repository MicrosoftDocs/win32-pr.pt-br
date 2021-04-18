---
description: Implementando IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementando IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506266"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementando IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

A classe de codificação no nível do quadro implementa essa interface para expor todos os blocos de metadados e solicitar o gravador de metadados apropriado para cada bloco. Se o formato de imagem der suporte a metadados globais, fora de qualquer quadro individual, você também deverá implementar essa interface na classe de codificador de nível de contêiner. Para obter uma discussão mais detalhada sobre manipuladores de metadados, consulte a seção sobre o [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) na seção sobre como implementar um decodificador de WIC-Enabled.

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

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa um [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) para inicializar o gravador de bloco. Você pode obter o **IWICMetadataBlockReader** do decodificador que decodificava a imagem.


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



Como inicializar o [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) com um [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instancia um gravador de metadados para cada leitor de metadados exposto pelo objeto **IWICMetadataBlockReader** , o aplicativo não precisa solicitar explicitamente um gravador para cada bloco de metadados.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) retorna o objeto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) para o enésimo bloco de metadados, em que n é o valor passado no parâmetro *nIndex* . Se não houver nenhum gravador de metadados registrado que possa manipular o tipo de metadados no enésimo bloco, a fábrica de componentes retornará o manipulador de metadados desconhecido, que tratará o bloco de metadados como um BLOB (objeto binário grande). Ele o serializará como um fluxo de bits sem tentar analisá-lo.

### <a name="addwriter"></a>AddWriter

O [**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permite que um chamador adicione um novo gravador de metadados. Isso será necessário se um aplicativo quiser adicionar metadados de um formato diferente dos blocos de metadados existentes. Por exemplo, um aplicativo pode querer adicionar alguns metadados XMP. Se não houver nenhum bloco de metadados XMP existente, o aplicativo deverá criar uma instância de um gravador de metadados XMP e usar o método **AddWriter** para incluí-lo na coleção de gravadores de metadados.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) é usado para adicionar um gravador de metadados em um índice específico na coleção. Se um gravador de metadados existir no momento nesse índice, o novo deverá substituí-lo.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) é usado para remover um gravador de metadados da coleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Instalação e registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



