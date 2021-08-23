---
title: Substituindo o aplicativo Windows visualizador de imagem e fax usando o verbo de visualização
description: A partir Windows XP, os usuários podem exibir, girar, imprimir e ampliar imagens.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows Visualizador de Imagem e Fax
- Verbo de visualização
- práticas recomendadas, Windows visualizador de imagem e fax
- práticas recomendadas, verbo de visualização
- performance,Windows Visualizador de Imagem e Fax
- performance,Preview verb
- register,Preview verb
- register,Slideshow verb
- Verbo de apresentação de slides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518e32f7b7bf33db26e534c92cfe2fb46c9a51bc444f04f4881f18fb1fe6c738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608516"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Substituindo o aplicativo Windows visualizador de imagem e fax usando o verbo de visualização

\[O recurso Visualizador de Imagem e Fax só tem suporte no Windows XP. \]

A partir Windows XP, os usuários podem exibir, girar, imprimir e ampliar imagens. Alguns desses recursos são fornecidos por meio do shell Windows e outros por meio do aplicativo Windows Visualizador de Imagens e Fax. Embora Windows Visualizador de Imagem e Fax fornece uma excelente linha de base de recursos e é uma parte importante da experiência de imagens, se você optar por, você poderá substituí-lo facilmente por um aplicativo diferente. Este documento foi projetado para ajudá-lo a substituir efetivamente o aplicativo Windows Visualizador de Imagens e Fax sem perder recursos importantes ou degradar a experiência do usuário.

-   [Práticas recomendadas](#best-practices)
    -   [Desempenho](#performance)
    -   [Recursos](#features)
    -   [Suporte ao formato](#format-support)
-   [Registrando para o verbo de visualização](#registering-for-the-preview-verb)
-   [Registrando para o verbo Editar](#registering-for-the-edit-verb)
-   [Registrando-se para o verbo apresentação de slides](#registering-for-the-slideshow-verb)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices"></a>Práticas Recomendadas

No Windows XP e posterior, o Shell inclui um verbo que você pode usar para permitir que os usuários visualizem imagens. Ele é chamado de *Visualização.* Esse verbo realça a tarefa principal do usuário para imagens, que está sendo visualizada. Para fazer com que essa experiência funcione bem, o aplicativo Windows Visualizador de Imagem e Fax possui a associação de visualização por padrão.

O Windows visualizador de imagem e fax, ou qualquer aplicativo que possui uma associação de arquivo, inclui um item que inicia o aplicativo de edição do usuário. Como o verbo Preview só é usado para visualizar imagens em vez de editá-las, seu aplicativo deve ter cuidado para seguir as recomendações neste documento ao reivindicar essa associação.

Você deseja garantir que um aplicativo que edite imagens ainda possa assumir o verbo Editar. Por exemplo, se um usuário tiver o Microsoft Picture It! instalado, ao clicar duas vezes em um arquivo .jpg, o computador deverá iniciar o aplicativo Windows Visualizador de Fax e Imagem. Mas, quando eles **clicarem em Editar** na barra de ferramentas, o computador deverá iniciar Imagem! com esse .jpg arquivo.

Há três considerações que você deve levar em conta ao substituir a imagem Windows e o Visualizador de Fax. Eles são:

-   [Desempenho](#performance)
-   [Recursos](#features)
-   [Suporte ao formato](#format-support)

### <a name="performance"></a>Desempenho

A principal consideração com o desempenho é a velocidade com que as imagens são carregadas. Embora nenhuma métrica de desempenho seja fornecida aqui, você deve tentar substituir Windows Visualizador de Imagem e Fax por um aplicativo que corresponde ou aumenta o desempenho.

O próprio aplicativo deve ser carregado rapidamente. Um dos principais problemas que os usuários experimentam com aplicativos que assumiam as associações de imagem é o tempo de espera enquanto o aplicativo é carregado. Isso geralmente ocorre quando um aplicativo de edição eficiente é carregado quando clica duas vezes em um arquivo de imagem, mesmo quando o usuário simplesmente deseja exibir o arquivo. É melhor para o usuário se você fornecer opções que as levam rapidamente para um aplicativo em que ele pode editar a imagem somente quando esse for o seu desejo.

### <a name="features"></a>Recursos

Há um conjunto mínimo de recursos que seu aplicativo deve fornecer ao substituir o aplicativo Windows Visualizador de Fax e Imagem. Elas são as seguintes:



| Recurso                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mostrar imagem na melhor opção             | Isso dá ao usuário a opção de ver toda a imagem dimensionada para o tamanho em que melhor me encaixa no espaço exibivel da janela do aplicativo. Dessa forma, eles podem ver toda a imagem, mesmo que ela seja ligeiramente degradada, diminuindo. Essa deve ser a configuração padrão sempre que uma imagem for carregada maior que o espaço exibivel. Caso contrário, a imagem deverá aparecer em seu tamanho real. Por exemplo, uma imagem de 64 x 64 pixels não deve ser dimensionada para um tamanho de 600 x 600 simplesmente porque esse é o tamanho da janela do aplicativo. |
| Mostrar imagem no tamanho real          | Isso dá ao usuário a opção de ver toda a imagem em sua resolução real. Isso permite que eles o vejam em seu tamanho apropriado e panoram sobre a imagem. Essa não deve ser a exibição padrão, a menos que a imagem seja menor que o espaço exibivel no aplicativo.                                                                                                                                                                                                                                                              |
| Ampliar a imagem                    | Isso permite que o usuário amplie uma parte da imagem para investigar detalhes mais finos ou simplesmente ampliar uma imagem pequena. Isso é semelhante a mostrar o tamanho real da imagem, mas permite que o usuário controle a proximidade com que ele exibe a imagem.                                                                                                                                                                                                                                                                                            |
| Reduzir a imagem                  | Isso permite que o usuário amplie e receba uma exibição mais ampla. Isso é semelhante a mostrar a imagem na melhor opção, mas permite que o usuário controle o quão distante ele exibe a imagem.                                                                                                                                                                                                                                                                                                                                                          |
| Próxima imagem                         | Isso permite que o usuário veja a próxima imagem na lista. Essa lista pode ser todas as imagens na pasta atual ou todas as imagens que o usuário seleciona como parte de uma operação de seleção multiseleção; ou seja, quando ele clica e arrasta para realçar imagens ou mantém o botão de controle pressionado e clica em arquivos individuais.                                                                                                                                                                                                                       |
| Imagem anterior                     | Isso permite que o usuário ex veja a imagem anterior na lista.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Girar no sentido horário 90 graus        | Isso permite que o usuário gire a imagem no sentido horário em trimestres. Windows O XP salva automaticamente a imagem quando ela a gira para reduzir a perda de qualidade da imagem. O aplicativo também pode girar incrementos menores, mas 90 graus é o padrão como a rotação mais comum para imagens digitais.                                                                                                                                                                                                                                 |
| Girar 90 graus no sentido anti-horário | Isso permite que o usuário gire a imagem no sentido anti-horário por trimestres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Imprimir                              | Isso permite que o usuário imprima a imagem que aparece no momento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Salvar como                            | Isso permite que o usuário salve a imagem em uma pasta especificada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Excluir imagem                       | Isso permite que o usuário exclua a imagem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ajuda                               | Isso fornece ao usuário a documentação de ajuda sobre o uso do aplicativo de exibição.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Propriedades                         | Isso permite que o usuário ex veja ou edite as propriedades da imagem, normalmente as informações de ARQUIVO de Imagem Permuta (EXIF) armazenadas em cada imagem.                                                                                                                                                                                                                                                                                                                                                                                      |
| Editar                               | Isso permite que o usuário iniciar seu programa de edição preferencial registrado para o verbo Editar na imagem.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Suporte ao formato

Como é difícil para um aplicativo dar suporte a todas as imagens diferentes, é recomendável que o aplicativo use Windows GDI+ para dar suporte a formatos de imagem. No entanto, se você optar por não usar GDI+, seu aplicativo deverá assumir apenas as associações de arquivo para as quais ele foi testado e é conhecido por funcionar. Em seguida, se o usuário precisar exibir um formato que você não trata, Windows Visualizador de Imagem e Fax ainda poderá fornecer acesso.

Por exemplo, Windows Visualizador de Imagem e Fax fornece várias ferramentas para editar anotações em imagens .tiff. A menos que essa funcionalidade seja duplicada em seu aplicativo, você não deve registrar seu aplicativo para manipular imagens .tiff. O princípio de condução deve ser garantir que o usuário não perca nenhuma funcionalidade.

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

Isso registra o aplicativo e o torna o aplicativo padrão para o verbo de visualização para um arquivo de .jpg. O seguinte também é necessário.

**HKEY \_ CLASSES \_ raiz** \\ **.jpg** \( padrão) = Application. jpeg

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

a partir do Windows Vista, um aplicativo também pode registrar o verbo de **apresentação de slides** . Os aplicativos que implementam uma apresentação de slides podem se registrar para serem invocados quando o verbo de apresentação de slides é escolhido. Esse registro é realizado exatamente da mesma maneira, conforme explicado para o verbo de visualização acima. É altamente recomendável que os aplicativos implementem a forma DropTarget do verbo. Dessa forma, eles podem passar um conjunto completo de itens. A implementação de DropTarget é registrada como mostrado aqui:

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

[Sobre GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 