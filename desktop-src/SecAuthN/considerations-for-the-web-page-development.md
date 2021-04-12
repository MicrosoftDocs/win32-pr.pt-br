---
description: O agente de autenticação da Web é criado na parte superior das mesmas tecnologias que alimentam o Internet Explorer no Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considerações para o desenvolvimento de páginas da Web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296850"
---
# <a name="considerations-for-the-web-page-development"></a>Considerações para o desenvolvimento de páginas da Web

O agente de autenticação da Web é criado na parte superior das mesmas tecnologias que alimentam o Internet Explorer no Windows. No entanto, devido a uma finalidade muito especial desse componente, alguns recursos do Internet Explorer foram desabilitados ou bloqueados para configuração específica. Além disso, o agente de autenticação da Web fornece um canal de log de eventos dedicado para ajudar a solucionar problemas com páginas que ele processa.

## <a name="internet-explorer-10-standard-document-mode"></a>Modo de documento padrão do Internet Explorer 10

O agente de autenticação da Web exibe todas as páginas no "modo de padrões IE10". Você pode usar as ferramentas de desenvolvedor no Internet Explorer para ver como sua página funciona em diferentes modos de documento. Para obter mais informações sobre a compatibilidade com o Internet Explorer 10, consulte os tópicos do MSDN para o [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Recursos desabilitados e bloqueados

Vários recursos do Internet Explorer são completamente desabilitados ou bloqueados para valores específicos que não podem ser alterados nas opções da Internet do sistema operacional.



| Recurso                            | Status                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API de cache de aplicativo ("AppCache") | Desabilitado                                                                                                                                                                                                        |
| Histórico de link                       | Desabilitado                                                                                                                                                                                                        |
| Arquivos temporários                    | habilitado                                                                                                                                                                                                         |
| Cookies                            | Os cookies de sessão estão habilitados. Cookies persistentes são permitidos, mas estão sujeitos a limpeza automática, a menos que o agente de autenticação da Web esteja no modo SSO. Para obter mais informações, consulte a seção logon único. |
| BD de índice                           | Desabilitado                                                                                                                                                                                                        |
| Armazenamento DOM                        | Desabilitado                                                                                                                                                                                                        |
| ActiveX                            | Desabilitado                                                                                                                                                                                                        |
| Downloads de arquivos                     | Desabilitado                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>Requisito de HTTPS

A primeira URL que um aplicativo usará para se comunicar com o provedor online precisa ser HTTPS.

## <a name="dimension-for-different-window-sizes"></a>Dimensão para diferentes tamanhos de janela

Um aplicativo do Windows 8 pode aparecer em vários tamanhos diferentes, como tela inteira, uma janela redimensionada ou dentro de um botão, como um botão de compartilhamento. Dependendo de qual layout da janela o agente de autenticação da Web aparece, o tamanho com o qual as páginas da Web precisam funcionar pode ser diferente. Para obter mais informações, consulte o tópico [diretrizes para redimensionamento para layouts estreitos](/previous-versions/windows/hh465371(v=win.10)) e o tópico [diretrizes para compartilhamento de conteúdo](/previous-versions/windows/hh465251(v=win.10)) .

A página da Web deve usar consultas de mídia do CSS para verificar o tamanho com o qual deve trabalhar e se ajustar de acordo. No entanto, a página não deve ser projetada com base nos pixels exatos documentados aqui e deve ser capaz de dimensionar para tamanhos diferentes. Os tamanhos especificados neste documento estão sujeitos a alterações em versões futuras do sistema operacional.

Se uma página não puder se ajustar a todas as informações no espaço alocado (por exemplo, uma longa lista de permissões que um aplicativo está solicitando), o agente de autenticação da Web fornecerá barras de rolagem para permitir que o usuário Role a página conforme necessário. O zoom também é fornecido pelo pinçar zoom para dispositivos baseados em toque e CTRL + roda do mouse para PCs desktop e laptop.

Para testar diferentes fatores de dimensionamento, use o [aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) carregado no Microsoft Visual Studio Professional 2012, que permite simular a tela inteira e os Estados redimensionados.

Além de layouts diferentes documentados acima, certifique-se de testar sua página em uma orientação de tela diferente (por exemplo, retrato e paisagem) e localidades e idiomas diferentes, bem como com recursos de acessibilidade, como a opção "tornar tudo maior" ativada.

Os layouts disponíveis são:

-   [Tela inteira](#full-screen)
-   [Janela redimensionada](#resized)
-   [Exibição de botão](#charm-view)
-   [Exibição do seletor de arquivos](#file-picker-view)

### <a name="full-screen"></a>Tela inteira

Para o layout de tela inteira, as dimensões da página da Web são:

-   Largura: 566 pixels
-   Altura: altura da tela (depende da resolução da tela)

O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web no layout de tela inteira.

![um exemplo de interface do usuário do agente de autenticação da Web no layout de tela inteira](images/wab-figure2.png)

### <a name="resized"></a>Redimensionado

Para uma janela redimensionada, as dimensões da página da Web podem ser:

-   Largura: 260 pixels
-   Altura: altura da tela (depende da resolução da tela)

O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web em uma janela redimensionada na página da Web do XBox. Observe que a interface do usuário do agente de autenticação da Web está apenas no lado direito da captura de tela.

![um exemplo de interface do usuário do agente de autenticação da Web em uma janela redimensionada](images/wab-figure3.png)

### <a name="charm-view"></a>Exibição de botão

Para a exibição de botão, as dimensões da página da Web são:

-   Largura: 566 pixels
-   Altura: altura da tela (depende da resolução da tela)

O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web na exibição de botão.

![um exemplo mostra a interface do usuário do agente de autenticação da Web na exibição de botão](images/wab-figure4.png)

### <a name="file-picker-view"></a>Exibição do seletor de arquivos

Para a exibição do seletor de arquivo, as dimensões da página da Web são:

-   Largura: 566 pixels
-   Altura: altura da tela (depende da resolução da tela)

O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web na exibição do seletor de arquivos.

![um exemplo mostra a interface do usuário do agente de autenticação da Web na exibição do seletor de arquivos](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>Nenhuma nova janela por padrão

Por padrão, nenhuma URL fará com que uma nova janela seja aberta, mas será exibida na janela do agente de autenticação da Web. Isso inclui o método de JavaScript Window. Open, o atributo "target" dos hiperlinks ou quando o usuário usa o mecanismo Ctrl + clique para forçar a abertura de uma nova janela. A exceção a essa regra é quando uma página da Web declara um link como seguro para ser navegado em um navegador, conforme descrito no destino de personalização dos hiperlinks.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
