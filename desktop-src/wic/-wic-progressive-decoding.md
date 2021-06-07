---
description: Este tópico apresenta a decodificação progressiva e como usar a decodificação progressiva em aplicativos.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Visão geral da decodificação progressiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b9708802b082a880f358b969d9dd4beb1e481
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443667"
---
# <a name="progressive-decoding-overview"></a>Visão geral da decodificação progressiva

Este tópico apresenta a decodificação progressiva e como usar a decodificação progressiva em aplicativos. Ele também fornece diretrizes para a criação de codecs que dão suporte à decodificação progressiva.

Este tópico inclui as seções a seguir.

-   [Introdução](#introduction)
-   [O que é decodificação progressiva?](#what-is-progressive-decoding)
-   [Suporte progressivo de decodificação no Windows 7](#progressive-decoding-support-in-windows-7)
-   [Decodificação progressiva de JPEG](#jpeg-progressive-decoding)
-   [Decodificação progressiva de PNG/GIF](#pnggif-progressive-decoding)
    -   [Decodificação progressiva de PNG](#png-progressive-decoding)
    -   [Decodificação progressiva de GIF](#gif-progressive-decoding)
-   [Decodificação progressiva em aplicativos](#progressive-decoding-in-applications)
-   [Suporte de codec personalizado para decodificação progressiva](#custom-codec-support-for-progressive-decoding)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

A decodificação progressiva fornece a capacidade de decodificar e renderizar de forma incremental partes de uma imagem antes de concluir o download da imagem inteira. Esse recurso melhora muito a experiência do usuário ao exibir imagens da Internet, pois o usuário não precisa aguardar a imagem inteira ser baixada antes que a decodificação possa começar. Os usuários podem ver uma visualização de imagem com os dados disponíveis por extenso antes que toda a imagem seja baixada. Esse recurso é essencial para qualquer aplicativo usado para exibir imagens da Internet ou de fontes de dados com largura de banda limitada.

O Windows Imaging Component (WIC) no Windows 7 oferece suporte à decodificação progressiva de formatos de imagem populares, como JPEG, PNG e GIF. O WIC também dá suporte a todos os codecs que não são da Microsoft habilitados para WIC que implementam a decodificação progressiva. Não há suporte para codificação progressiva na versão atual do WIC. Este tópico descreve a decodificação progressiva no Windows 7 e o procedimento para habilitar a decodificação progressiva em seus aplicativos.

## <a name="what-is-progressive-decoding"></a>O que é decodificação progressiva?

A decodificação progressiva é a capacidade de decodificar incrementalmente partes de uma imagem de um arquivo de imagem incompleto. A decodificação tradicional requer um arquivo de imagem completo antes que a decodificação possa começar. A decodificação progressiva começa após a conclusão do download de um nível progressivo de uma imagem. O decodificador executa uma passagem de decodificação no nível progressivo atual da imagem. Em seguida, ele executa vários passos de decodificação na imagem à medida que cada nível progressivo é baixado. Cada passagem de decodificação revela mais da imagem até que a imagem seja totalmente baixada e decodificada. O número de passagens necessárias para decodificar uma imagem completa depende do formato do arquivo de imagem e do processo de codificação usado para criar a imagem.

As imagens devem ser codificadas especificamente para implementar a decodificação progressiva, mas nem todos os formatos de imagem dão suporte a ela. A lista a seguir resume os requisitos para usar a decodificação progressiva.

-   O arquivo de imagem deve dar suporte à decodificação progressiva. A maioria dos formatos de imagem não oferece suporte à decodificação progressiva, embora os formatos de imagem populares JPEG, PNG e GIF façam.
-   O arquivo de imagem deve ser codificado como uma imagem progressiva. Os arquivos de imagem que não foram criados com a codificação de imagem progressiva não podem implementar a decodificação progressiva, mesmo onde o formato de arquivo seria compatível.
-   Um codec que dá suporte à decodificação progressiva deve estar disponível. Se um codec não oferecer suporte à decodificação progressiva, uma imagem codificada como uma imagem progressiva será decodificada como uma imagem tradicional.

## <a name="progressive-decoding-support-in-windows-7"></a>Suporte progressivo de decodificação no Windows 7

O Windows 7 fornece codecs internos que dão suporte à decodificação progressiva para formatos de imagem JPEG, PNG e GIF. Cada um desses codecs do Windows 7 executa vários passos de decodificação em uma imagem. Cada passagem corresponde a um nível específico e a uma parte da imagem decodificada, eventualmente levando a uma imagem totalmente decodificada.

Cada formato de imagem manipula a decodificação progressiva de maneira diferente. A tabela a seguir fornece informações sobre o número de níveis progressivos e o método de decodificação com suporte nos formatos de decodificação progressiva do Windows 7. 

| Formato de imagem | Número de níveis progressivos com suporte | Método de decodificação progressiva |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definido pela imagem                       | Aumentando a resolução       |
| PNG          | 7                                      | Entrelaça                 |
| GIF          | 4                                      | Entrelaça                 |



 

Além disso, a decodificação progressiva pode ser implementada em codecs fornecendo suporte para interfaces e métodos progressivos. Se a decodificação progressiva não for suportada em um codec, as mensagens de erro apropriadas deverão ser retornadas se esses métodos forem chamados.

## <a name="jpeg-progressive-decoding"></a>Decodificação progressiva de JPEG

A decodificação progressiva de JPEG apresenta dados de imagem em resoluções cada vez maiores para cada nível, até que a imagem de resolução completa esteja disponível. Cada nível da imagem é definido para fornecer um nível de resolução diferente. À medida que mais níveis progressivos são disponibilizados, a imagem é exibida em resoluções mais altas, até que a imagem de resolução completa seja resolvida.

O número de níveis disponíveis e a resolução definida em cada nível depende inteiramente do JPEG codificado. As duas imagens a seguir mostram um exemplo de decodificação progressiva de JPEG em dois níveis progressivos.

![exemplos de decodificação progressiva de JPEG](graphics/Progressive_JPEG_Comparison.jpg)

A imagem à esquerda é decodificada no nível progressivo 0. A imagem à direita é totalmente decodificada após cinco níveis progressivos.

## <a name="pnggif-progressive-decoding"></a>Decodificação progressiva de PNG/GIF

A decodificação progressiva de PNG e GIF usa um método de decodificação progressivo entrelaçado. O processo de decodificação para ambos os formatos é muito semelhante.

### <a name="png-progressive-decoding"></a>Decodificação progressiva de PNG

Os arquivos de imagem PNG fornecem sete níveis progressivos para decodificação, conforme descrito na especificação de PNG. A decodificação progressiva de PNG é implementada decodificando um padrão especificado de pixels em cada passagem do decodificador. O padrão na tabela a seguir da especificação PNG é replicado sobre toda a imagem. Cada número representa o nível progressivo no qual o pixel correspondente será decodificado.



|  &nbsp;  |  &nbsp;   |  &nbsp;   |  &nbsp;   |   &nbsp;  |  &nbsp;   |  &nbsp;   | &nbsp;    |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

Na tabela acima, você pode determinar os pixels que serão decodificados com cada passagem do decodificador. Ao contrário do codec GIF do Windows 7, o codec PNG do Windows 7 Replica o pixel mais disponível à esquerda em uma linha de exame para popular pixels vazios.

As imagens a seguir mostram um exemplo do codec de decodificação progressiva do PNG do Windows 7 em três níveis progressivos.

![exemplos de decodificação progressiva de png](graphics/PNG_Progressive_Comparison.jpg)

A imagem na parte superior esquerda mostra uma imagem PNG decodificada no nível progressivo 0. A imagem superior direita mostra a mesma imagem PNG decodificada no nível progressivo 3. A imagem inferior mostra a mesma imagem totalmente decodificada após 7 níveis progressivos.

### <a name="gif-progressive-decoding"></a>Decodificação progressiva de GIF

Os arquivos de imagem GIF fornecem quatro níveis progressivos para decodificação, conforme descrito na especificação GIF. Cada passagem popula determinadas linhas em uma imagem, produzindo uma imagem completa após a quarta passagem. A tabela a seguir da especificação GIF mostra quais linhas de verificação são decodificadas por cada passagem do decodificador. 

| Número de nível/número de passagem | Linhas de verificação preenchidas   | Iniciando linha de varredura |
|---------------------------|------------------------|--------------------|
| 1                         | Toda oitava linha de varredura | 0                  |
| 2                         | Toda oitava linha de varredura | 4                  |
| 3                         | A cada quarta linha de varredura | 2                  |
| 4                         | Toda segunda linha de varredura | 1                  |



 

Embora os codecs possam especificar o conteúdo de pixels vazios em qualquer nível específico, o codec GIF do Windows popula as linhas de digitalização vazias replicando as linhas de digitalização preenchidas acima da linha de varredura vazia.

## <a name="progressive-decoding-in-applications"></a>Decodificação progressiva em aplicativos

A interface de decodificação progressiva principal é a interface [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) . Para obter uma referência à interface, consulte um quadro de imagem ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) para **IWICProgressiveLevelControl**. Os métodos progressivos podem ser acessados a partir da interface.

O código a seguir fornece um exemplo para usar a decodificação progressiva em aplicativos.


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



O código anterior fornece a funcionalidade básica necessária para implementar a decodificação progressiva na maioria dos aplicativos. Usando o código, os níveis progressivos podem ser acessados como dados de pixel de imagem ficam disponíveis. A função [**SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) bloqueia a execução até que o nível solicitado esteja disponível.

## <a name="custom-codec-support-for-progressive-decoding"></a>Suporte de codec personalizado para decodificação progressiva

Os desenvolvedores de codec podem optar por implementar o [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) se seus formatos de imagem oferecerem suporte à decodificação progressiva. O suporte para decodificação progressiva não é um requisito para descoberta e arbitragem pelo WIC. No entanto, a decodificação progressiva aprimora muito a experiência do usuário e a implementação deve ser considerada se possível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Compactação e codificação digitais de Continuous-Tone imagens ainda-requisitos e diretrizes](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[Formato de intercâmbio de arquivos JPEG](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[Especificação de GIF89a](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Especificação e extensões PNG (Portable Network Graphics)](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



