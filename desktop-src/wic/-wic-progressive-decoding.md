---
description: Este tópico apresenta a decodificação progressiva e como usar a decodificação progressiva em aplicativos.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Visão geral da decodificação progressiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a409a337ecd3852a50cb5ca1a410ebd32c7f3226c79aacca20b10733e214fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710031"
---
# <a name="progressive-decoding-overview"></a>Visão geral da decodificação progressiva

Este tópico apresenta a decodificação progressiva e como usar a decodificação progressiva em aplicativos. Ele também fornece diretrizes para criar codecs que suportam decodificação progressiva.

Este tópico inclui as seções a seguir.

-   [Introdução](#introduction)
-   [O que é Decodificação Progressiva?](#what-is-progressive-decoding)
-   [Suporte à decodificação progressiva Windows 7](#progressive-decoding-support-in-windows-7)
-   [Decodificação progressiva jpeg](#jpeg-progressive-decoding)
-   [Decodificação progressiva de PNG/GIF](#pnggif-progressive-decoding)
    -   [Decodificação progressiva de PNG](#png-progressive-decoding)
    -   [Decodificação progressiva gif](#gif-progressive-decoding)
-   [Decodificação progressiva em aplicativos](#progressive-decoding-in-applications)
-   [Suporte a codec personalizado para decodificação progressiva](#custom-codec-support-for-progressive-decoding)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

A decodificação progressiva fornece a capacidade de decodificar incrementalmente e renderizar partes de uma imagem antes que toda a imagem termine de ser baixada. Esse recurso melhora muito a experiência do usuário ao exibir imagens da Internet, pois o usuário não precisa aguardar o download da imagem inteira antes que a decodificação possa começar. Os usuários podem ver uma visualização de imagem com os dados disponíveis muito antes que toda a imagem seja baixada. Esse recurso é essencial para qualquer aplicativo usado para exibir imagens da Internet ou de fontes de dados com largura de banda limitada.

O WIC (Windows Imaging Component) do Windows 7 dá suporte à decodificação progressiva de formatos de imagem populares, como JPEG, PNG e GIF. O WIC também dá suporte a quaisquer codecs não Microsoft habilitados para WIC que implementam a decodificação progressiva. Não há suporte para codificação progressiva na versão atual do WIC. Este tópico descreve a decodificação progressiva no Windows 7 e o procedimento para habilenciar a decodificação progressiva em seus aplicativos.

## <a name="what-is-progressive-decoding"></a>O que é Decodificação Progressiva?

A decodificação progressiva é a capacidade de decodificar incrementalmente partes de uma imagem de um arquivo de imagem incompleto. A decodificação tradicional requer um arquivo de imagem completo antes que a decodificação possa começar. A decodificação progressiva é iniciada após o download de um nível progressivo de uma imagem. O decodificador executa uma passagem de decodificação no nível progressivo atual da imagem. Em seguida, ele executa várias passagens de decodificação na imagem conforme cada nível progressivo é baixado. Cada passagem de decodificação revela mais da imagem até que a imagem seja totalmente baixada e decodificada. O número de passagens necessárias para decodificar uma imagem completa depende do formato de arquivo de imagem e do processo de codificação usado para criar a imagem.

As imagens devem ser codificadas especificamente para implementar a decodificação progressiva, mas nem todos os formatos de imagem são suportados. A lista a seguir resume os requisitos para usar a decodificação progressiva.

-   O arquivo de imagem deve dar suporte à decodificação progressiva. A maioria dos formatos de imagem não é suportada pela decodificação progressiva, embora os formatos de imagem populares JPEG, PNG e GIF deem.
-   O arquivo de imagem deve ser codificado como uma imagem progressiva. Arquivos de imagem que não foram criados com a codificação de imagem progressiva não podem implementar a decodificação progressiva, mesmo em que o formato de arquivo seria suportado de outra forma.
-   Um codec que dá suporte à decodificação progressiva deve estar disponível. Se um codec não dá suporte à decodificação progressiva, uma imagem codificada como uma imagem progressiva será decodificada como uma imagem tradicional.

## <a name="progressive-decoding-support-in-windows-7"></a>Suporte à decodificação progressiva Windows 7

Windows 7 fornece codecs integrados que suportam decodificação progressiva para formatos de imagem JPEG, PNG e GIF. Cada um desses Windows 7 codecs executam várias passagens de decodificação em uma imagem. Cada passagem corresponde a um nível específico e parte da imagem que é decodificada, eventualmente levando a uma imagem totalmente decodificada.

Cada formato de imagem lida com a decodificação progressiva de uma maneira diferente. A tabela a seguir fornece informações sobre o número de níveis progressivos e o método de decodificação com suporte pelos formatos de decodificação Windows 7 progressivos. 

| Formato de imagem | Número de níveis progressivos com suporte | Método de decodificação progressiva |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definido por Imagem                       | Aumentar a resolução       |
| PNG          | 7                                      | Entrelaçamento                 |
| GIF          | 4                                      | Entrelaçamento                 |



 

Além disso, a decodificação progressiva pode ser implementada em codecs fornecendo suporte para interfaces e métodos progressivos. Se a decodificação progressiva não tiver suporte em um codec, as mensagens de erro apropriadas deverão ser retornadas se esses métodos são chamados.

## <a name="jpeg-progressive-decoding"></a>Decodificação progressiva jpeg

A decodificação progressiva jpeg apresenta dados de imagem em resoluções cada vez mais altas para cada nível, até que a imagem de resolução completa seja disponibilizada. Cada nível da imagem é definido para fornecer um nível de resolução diferente. À medida que níveis mais progressivos ficam disponíveis, a imagem é exibida em resoluções mais altas, até que a imagem de resolução completa seja resolvida.

O número de níveis disponíveis e o conjunto de resolução em cada nível depende inteiramente do JPEG codificado. As duas imagens a seguir mostram um exemplo de decodificação progressiva jpeg em dois níveis progressivos.

![exemplos de decodificação progressiva jpeg](graphics/Progressive_JPEG_Comparison.jpg)

A imagem à esquerda é decodificada no nível progressivo 0. A imagem à direita é totalmente decodificada após cinco níveis progressivos.

## <a name="pnggif-progressive-decoding"></a>Decodificação progressiva de PNG/GIF

A decodificação progressiva de PNG e GIF usa um método de decodificação progressiva entrelaçado. O processo de decodificação para ambos os formatos é muito semelhante.

### <a name="png-progressive-decoding"></a>Decodificação progressiva de PNG

Os arquivos de imagem PNG fornecem sete níveis progressivos para decodificação, conforme descrito na especificação PNG. A decodificação progressiva de PNG é implementada decodificando um padrão especificado de pixels em cada passagem do decodificador. O padrão na tabela a seguir da especificação PNG é replicado em toda a imagem. Cada número representa o nível progressivo no qual o pixel correspondente será decodificado.



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



 

Na tabela acima, você pode determinar os pixels que serão decodificados com cada passagem do decodificador. ao contrário do codec GIF Windows 7, o codec de PNG Windows 7 replica o pixel mais disponível à esquerda em uma linha de exame para popular pixels vazios.

as imagens a seguir mostram um exemplo do codec de decodificação progressiva do PNG Windows 7 em três níveis progressivos.

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



 

embora os codecs possam especificar o conteúdo de pixels vazios em qualquer nível específico, o codec Windows GIF popula as linhas de digitalização vazias, replicando as linhas de digitalização preenchidas acima da linha de varredura vazia.

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

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
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

 

 



