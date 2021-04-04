---
title: Substituindo o aplicativo Windows Picture and Fax Viewer usando o verbo Preview
description: A partir do Windows XP, os usuários podem exibir, girar, imprimir e aplicar zoom em imagens.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Visualizador de imagens e fax do Windows
- Verbo de visualização
- práticas recomendadas, visualizador de imagens e fax do Windows
- práticas recomendadas, verbo de visualização
- desempenho, visualizador de imagens e fax do Windows
- desempenho, verbo de visualização
- registrar, Visualizar verbo
- registro, verbo de apresentação de slides
- Verbo de apresentação de slides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6769e13aaea41b3b05bbf674ea95d7f88fb646
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917308"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Substituindo o aplicativo Windows Picture and Fax Viewer usando o verbo Preview

\[O recurso Visualizador de imagem e fax tem suporte apenas no Windows XP. \]

A partir do Windows XP, os usuários podem exibir, girar, imprimir e aplicar zoom em imagens. Alguns desses recursos são fornecidos por meio do shell do Windows e outros por meio do aplicativo Windows Picture and Fax Viewer. Embora o Visualizador de imagens e fax do Windows forneça uma excelente linha de base de recursos e seja uma parte fundamental da experiência de geração de imagens, se você optar por fazê-lo, poderá substituí-lo facilmente por um aplicativo diferente. Este documento foi criado para ajudá-lo a substituir efetivamente o aplicativo Windows Picture and Fax Viewer sem perder recursos importantes ou degradar a experiência do usuário.

-   [Práticas recomendadas](#best-practices)
    -   [Desempenho](#performance)
    -   [Recursos](#features)
    -   [Suporte de formato](#format-support)
-   [Registrando para o verbo de visualização](#registering-for-the-preview-verb)
-   [Registrando para o verbo editar](#registering-for-the-edit-verb)
-   [Registrando para o verbo de apresentação de slides](#registering-for-the-slideshow-verb)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices"></a>Práticas Recomendadas

No Windows XP e posterior, o Shell inclui um verbo que você pode usar para permitir que os usuários visualizem imagens. Ele é chamado de *Visualização*. Esse verbo realça a tarefa principal do usuário para imagens, que está sendo exibida. Para que essa experiência funcione bem, o aplicativo visualizador de imagens e fax do Windows possui a associação de visualização por padrão.

O Visualizador de imagens e fax do Windows, ou qualquer aplicativo que possui uma associação de arquivo, inclui um item que inicia o aplicativo de edição do usuário. Como o verbo Preview é usado apenas para visualizar imagens em vez de editá-los, seu aplicativo deve ter cuidado para seguir as recomendações neste documento ao reivindicar essa associação.

Você deseja garantir que um aplicativo que edita imagens ainda possa assumir o verbo de edição. Por exemplo, se um usuário tiver o Microsoft Picture It! instalado, ao clicar duas vezes em um arquivo. jpg, o computador deverá iniciar o aplicativo do Visualizador de imagens e fax do Windows. Mas, quando eles clicarem em **Editar** na barra de ferramentas, o computador deverá iniciar o Picture It! com esse arquivo. jpg.

Há três considerações que você deve levar em conta ao substituir o Visualizador de imagens e fax do Windows. Eles são:

-   [Desempenho](#performance)
-   [Recursos](#features)
-   [Suporte de formato](#format-support)

### <a name="performance"></a>Desempenho

A principal consideração com o desempenho é a velocidade na qual as imagens são carregadas. Embora nenhuma métrica de desempenho seja fornecida aqui, você deve tentar substituir o Visualizador de imagens e fax do Windows por um aplicativo que corresponda ou aumente o desempenho.

O próprio aplicativo deve ser carregado rapidamente. Um dos principais problemas que os usuários enfrentam com os aplicativos que assumem as associações de imagem é o tempo de espera durante o carregamento do aplicativo. Isso geralmente resulta da carga de um aplicativo de edição eficiente quando clica duas vezes em um arquivo de imagem, mesmo quando o usuário simplesmente deseja exibir o arquivo. É melhor para o usuário se você fornecer opções que as levam rapidamente a um aplicativo no qual eles podem editar a imagem somente quando essa for sua desejar.

### <a name="features"></a>Recursos

Há um conjunto mínimo de recursos que seu aplicativo deve fornecer ao substituir o aplicativo Windows Picture and Fax Viewer. Elas são as seguintes:



| Recurso                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mostrar imagem no melhor ajuste             | Isso dá ao usuário a opção de ver toda a imagem dimensionada para o tamanho em que melhor se ajusta ao espaço visível da janela do aplicativo. Dessa forma, eles podem ver a imagem inteira, mesmo que seja um pouco degradado com o zoom. Essa deve ser a configuração padrão sempre que uma imagem é carregada que é maior do que o espaço visível. Caso contrário, a imagem deve aparecer em seu tamanho real. Por exemplo, uma imagem de pixel de 64 x 64 não deve ser dimensionada para um tamanho de 600 x 600 simplesmente porque esse é o tamanho da janela do aplicativo. |
| Mostrar imagem em tamanho real          | Isso dá ao usuário a opção de ver toda a imagem em sua resolução real. Isso permite que eles o exibam com seu tamanho apropriado e panorâmica sobre a imagem. Essa não deve ser a exibição padrão, a menos que a imagem seja menor do que o espaço visível no aplicativo.                                                                                                                                                                                                                                                              |
| Ampliar imagem                    | Isso permite que o usuário Aplique zoom em uma parte da imagem para investigar os detalhes mais definados ou simplesmente aumentar uma imagem pequena. Isso é semelhante a mostrar o tamanho real da imagem, mas permite que o usuário controle o quanto eles exibem a imagem.                                                                                                                                                                                                                                                                                            |
| Reduzir da imagem                  | Isso permite que o usuário reduza e obtenha uma visão mais ampla. Isso é semelhante a mostrar a imagem no melhor ajuste, mas permite que o usuário controle a distância de exibição da imagem.                                                                                                                                                                                                                                                                                                                                                          |
| Próxima imagem                         | Isso permite que o usuário veja a próxima imagem na lista. Essa lista pode ser todas as imagens na pasta atual ou todas as imagens que o usuário seleciona como parte de uma operação de seleção ascada; ou seja, quando ele clica e arrasta para realçar imagens ou mantém o botão de controle e clica em arquivos individuais.                                                                                                                                                                                                                       |
| Imagem anterior                     | Isso permite que o usuário exiba a imagem anterior na lista.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Girar no sentido horário 90 graus        | Isso permite que o usuário gire a imagem no sentido horário em trimestres. O Windows XP salva automaticamente a imagem quando a gira para reduzir a perda de qualidade da imagem. O aplicativo também pode girar incrementos menores, mas 90 graus é o padrão como a rotação mais comum para imagens digitais.                                                                                                                                                                                                                                 |
| Girar no sentido anti-horário 90 graus | Isso permite que o usuário gire a imagem no sentido anti-horário por trimestres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Imprimir                              | Isso permite que o usuário imprima a imagem que aparece atualmente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Salvar como                            | Isso permite que o usuário salve a imagem em uma pasta especificada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Excluir imagem                       | Isso permite que o usuário exclua a imagem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ajuda                               | Isso fornece ao usuário a documentação de ajuda sobre o uso do aplicativo de exibição.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Propriedades                         | Isso permite que o usuário exiba ou edite as propriedades da imagem, normalmente as informações de EXIF (arquivo de imagem intercambiável) armazenadas em cada imagem.                                                                                                                                                                                                                                                                                                                                                                                      |
| Editar                               | Isso permite que o usuário inicie seu programa de edição preferencial registrado para o verbo editar na imagem.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Suporte de formato

Como é difícil para um aplicativo dar suporte a todas as imagens diferentes, é recomendável que o aplicativo use o Windows GDI+ para oferecer suporte a formatos de imagem. No entanto, se você optar por não usar o GDI+, seu aplicativo deverá assumir apenas as associações de arquivo para as quais ele foi testado e se sabe que funciona. Em seguida, se o usuário precisar exibir um formato que você não manipula, o Visualizador de imagens e fax do Windows ainda poderá fornecer acesso.

Por exemplo, o Visualizador de imagens e fax do Windows fornece várias ferramentas para editar anotações em imagens. TIFF. A menos que essa funcionalidade seja duplicada em seu aplicativo, você não deve registrar seu aplicativo para manipular imagens. TIFF. O princípio de condução deve ser garantir que o usuário não perca nenhuma funcionalidade.

## <a name="registering-for-the-preview-verb"></a>Registrando para o verbo de visualização

Registrar um aplicativo para manipular o verbo de visualização é bem simples. Localize o seguinte valor do aplicativo no registro, em que Application. jpeg representa o nome da chave de associação de arquivo do aplicativo (consulte os [programas padrão](/windows/desktop/shell/default-programs) para obter mais detalhes):

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Altere o nome da subchave **aberta** para "Preview", conforme mostrado aqui.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Isso registra o aplicativo e o torna o aplicativo padrão para o verbo de visualização para um arquivo. jpg. O seguinte também é necessário.

**HKEY \_ CLASSES \_ root** \\ **. jpg** \( padrão) = Application. jpeg

## <a name="registering-for-the-edit-verb"></a>Registrando para o verbo editar

Isso registra um aplicativo para o verbo editar e o torna o novo aplicativo padrão para editar uma imagem. O aplicativo registrado deve assumir o recurso de edição do aplicativo padrão existente no momento da instalação e instalá-lo novamente como o manipulador no momento da desinstalação. Isso pode ser feito registrando o novo aplicativo no nível da lista de associação do que o aplicativo padrão. O aplicativo padrão é registrado aqui:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

O novo aplicativo deve ser registrado aqui:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Registrando para o verbo de apresentação de slides

A partir do Windows Vista, um aplicativo também pode registrar o verbo de **apresentação de slides** . Os aplicativos que implementam uma apresentação de slides podem se registrar para serem invocados quando o verbo de apresentação de slides é escolhido. Esse registro é realizado exatamente da mesma maneira, conforme explicado para o verbo de visualização acima. É altamente recomendável que os aplicativos implementem a forma DropTarget do verbo. Dessa forma, eles podem passar um conjunto completo de itens. A implementação de DropTarget é registrada como mostrado aqui:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         slideshow
            DropTarget
               CLSID = {CLSID of the implementation}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução às associações de arquivo](/windows/desktop/shell/fa-intro)
</dt> <dt>

[Sobre o GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 