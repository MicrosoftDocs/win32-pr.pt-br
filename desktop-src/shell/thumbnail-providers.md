---
description: O Windows Vista faz mais uso de imagens em miniaturas específicas de arquivo do que as versões anteriores do Windows.
title: Manipuladores de miniatura
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171173"
---
# <a name="thumbnail-handlers"></a>Manipuladores de miniatura

O Windows Vista faz mais uso de imagens em miniaturas específicas de arquivo do que as versões anteriores do Windows. O Windows Vista os usa em todas as exibições, em caixas de diálogo e em qualquer tipo de arquivo que as forneça. Outros aplicativos também podem consumir sua miniatura. A exibição de miniatura também foi alterada. Agora, um espectro contínuo de tamanhos selecionáveis pelo usuário está disponível em vez de tamanhos discretos, como ícones e miniaturas fornecidos no Windows XP.

> [!Note]  
> Você pode ouvir essas miniaturas conhecidas como ícones dinâmicos.

 

As miniaturas de resolução de 32 bits e tão grandes quanto 256x256 pixels geralmente são usadas na interface do usuário do Windows Vista. Os proprietários de formato de arquivo devem estar preparados para exibir suas miniaturas nesse tamanho. Eles também devem fornecer imagens não estáticas para suas miniaturas que refletem o conteúdo do arquivo específico. Por exemplo, a miniatura de um arquivo de texto deve mostrar uma versão em miniatura do documento, incluindo seu texto.

A interface [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) foi introduzida para tornar o fornecimento de uma miniatura mais fácil e mais simples do que no passado, quando [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) teria sido usado em vez disso. Observe que o código existente que usa **IExtractImage** ainda é válido no Windows Vista. No entanto, não há suporte para **IExtractImage** no painel de **detalhes** .

Este tópico aborda o seguinte:

-   [Processos de miniatura](#thumbnail-processes)
-   [Cache e dimensionamento de miniatura](#thumbnail-cache-and-sizing)
-   [Sobreposições de miniatura](#thumbnail-overlays)
-   [Adornos de miniatura](#thumbnail-adornments)
-   [Registrando seu manipulador de miniaturas](#registering-your-thumbnail-handler)
-   [Tópicos relacionados](#related-topics)

## <a name="thumbnail-processes"></a>Processos de miniatura

Manipuladores, incluindo manipuladores de miniatura, são executados por padrão em um processo separado. Você pode forçar o manipulador a ser executado em processo passando um valor **nulo** como o contexto de associação em uma chamada para [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) , conforme mostrado aqui:


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



Você também pode recusar a execução fora do processo por padrão definindo a entrada DisableProcessIsolation no registro, conforme mostrado neste exemplo. O CLSID (identificador de classe) {E357FCCD-A995-4576-B01F-234630154E96} é o CLSID para implementações de [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Cache e dimensionamento de miniatura

Quando uma miniatura é necessária, o Windows verifica primeiro o cache de miniaturas da imagem. O extrator de miniatura será chamado se a imagem não for encontrada no cache. Ele também é chamado quando a hora da última modificação da imagem é posterior àquela da cópia no cache.

As imagens em miniatura nesse cache são armazenadas em um conjunto de tamanhos discretos. Todos os tamanhos são fornecidos em pixels.

-   32x32
-   96x96
-   256x256
-   1024x1024

> [!Note]  
> Esses valores estão sujeitos a alterações. O código não deve pressupor que qualquer tamanho específico sempre será usado.

 

Se uma imagem não for quadrada, você não deverá fazê-la por conta própria. O Windows é responsável por respeitar a taxa de proporção original e preencher a imagem para um tamanho quadrado.

Quando uma imagem de um determinado tamanho é solicitada, a menos que uma correspondência exata seja encontrada, o Windows Vista sempre recupera a próxima imagem maior e a dimensiona para o tamanho solicitado. Uma imagem nunca é dimensionada em tamanho, como era o caso nas versões anteriores do Windows.

A tabela a seguir fornece alguns exemplos da relação entre o tamanho solicitado e o tamanho disponível.



| Tamanho máximo da imagem que você fornece | Tamanho solicitado pelo extrator | Você fornece                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156x120                        | 256x256                         | 156x120 (não preencha, mantenha a taxa de proporção) |
| 2048x1024                      | 256x256                         | 256x128 (não preencha, mantenha a taxa de proporção) |



 

Você pode declarar um ponto de corte como parte da entrada de ID do programa do aplicativo associado no registro. Abaixo desse tamanho, as miniaturas não são usadas.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

A entrada ThumbnailCutoff é um desses valores de REG \_ DWORD.

| Valor | Corte | HighDPI confidencial |
|-------|--------|-------------------|
| 0     | 32x32  | Sim               |
| 1     | 16x16  | Yes               |
| 2     | 48 x 48  | Yes               |
| 3     | 16x16  | Yes               |


A sensibilidade de pontos por polegada (DPI) alta significa que as dimensões de pixel da miniatura se ajustam automaticamente para o dpi maior. Por exemplo, uma imagem 32x32 em 96 DPI seria uma imagem 40x40 em 120 dpi.

Se a entrada ThumbnailCutoff não for especificada, o corte padrão será 20x20 (não diferencia DPI).

## <a name="thumbnail-overlays"></a>Sobreposições de miniatura

Sobreposições de miniatura, uma imagem pequena exibida no canto inferior direito da miniatura, fornecem uma oportunidade para que os desenvolvedores apliquem identificação de marca às suas miniaturas. As sobreposições são declaradas no registro como parte da entrada da ID do programa do aplicativo associado, como mostrado aqui:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

A entrada TypeOverlay contém um valor de REG \_ sz interpretado da seguinte maneira:

-   Se o valor for uma referência de recurso (um arquivo **. ico** inserido na DLL), como `ISVComponent.dll,-155` , essa imagem será usada como a sobreposição de arquivos com essa extensão de nome de arquivo. Observe que, neste exemplo, **155** é a ID de recurso e, se a dll não estiver presente em um caminho padrão (como **C:/Windows/system32**), o caminho completo será necessário em vez de apenas o nome da dll.
-   Se o valor for uma cadeia de caracteres vazia, nenhuma sobreposição será aplicada à imagem.
-   Se o valor não estiver presente, será usado o ícone padrão do aplicativo associado.

Sobreposições para suas miniaturas só devem ser fornecidas por meio desse mecanismo e aplicadas pelo Windows. Não aplique sobreposições por conta própria.

## <a name="thumbnail-adornments"></a>Adornos de miniatura

Adorners como drop Shadows são aplicados a miniaturas com base no tema selecionado no momento. Os adornos são fornecidos pelo Windows; Não os crie por conta própria. O Windows poderia alterar a aparência de adorners específicos a qualquer momento, portanto, se você tiver fornecido a sua conta, correria o risco de ficar fora de sincronia com o sistema. As miniaturas podem ficar com uma aparência de data ou fora do local.

Adornos potenciais são declarados no registro como parte da entrada de ID do programa do aplicativo associado, como mostrado aqui:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

A entrada de tratamento contém um desses valores de REG \_ DWORD:



| Valor | Significado         |
|-------|-----------------|
| 0     | Sem Adornment    |
| 1     | Sombra     |
| 2     | Borda da foto    |
| 3     | Sobrerockets de vídeo |


Uma sombra suspensa é aplicada a imagens por padrão.

## <a name="registering-your-thumbnail-handler"></a>Registrando seu manipulador de miniaturas

O registro de um manipulador de miniaturas baseia-se nas associações de arquivo padrão.

O GUID para a extensão do shell do manipulador de miniaturas é `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Criando manipuladores de miniatura](building-thumbnail-providers.md)
</dt> <dt>

[Diretrizes do manipulador de miniaturas](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



