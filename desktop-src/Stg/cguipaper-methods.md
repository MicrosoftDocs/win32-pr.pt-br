---
title: Métodos CGuiPaper
description: Os métodos de CGuiPaper são resumidos da seguinte maneira. Esses métodos são todos implementados no GUIPAPER. CPP.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1303ca38ffe02da0dc747e1a8834d36419452209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635137"
---
# <a name="cguipaper-methods"></a>Métodos CGuiPaper

Os métodos de CGuiPaper são resumidos da seguinte maneira. Esses métodos são todos implementados no GUIPAPER. CPP.



| Método                                                         | Descrição                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL init (HINSTANCE hInst, HWND hWnd, TCHAR \* pszCmdLineFile); | Inicializa o GuiPaper. Solicita que o servidor crie um objeto de copapel.                                                     |
| HRESULT Drawe (void);                                          | Bloqueia o papel para desenhar exclusivamente por este cliente.                                                                   |
| HRESULT DrawOff (void);                                         | Desbloqueia o papel para permitir que outros clientes desenhem.                                                                         |
| HRESULT ClearWin (void);                                        | Limpa a janela de exibição, mas retém os dados de tinta.                                                                           |
| HRESULT PaintWin (void);                                        | Limpa a janela e repinta com os dados de tinta atuais.                                                                     |
| HRESULT Erase (void);                                           | Apaga o conteúdo do desenho atual e limpa a janela de exibição.                                                             |
| Redimensionamento de HRESULT (WORD wWidth, WORD wHeight);                     | Redimensiona a janela de exibição.                                                                                           |
| HRESULT InkWidth (curto nInkWidth);                             | Define a largura da tinta atual para o desenho.                                                                                   |
| HRESULT InkColor (COLORREF crInkColor);                         | Define a cor da tinta atual para o desenho.                                                                                   |
| HRESULT InkSaving (BOOL bInkSaving);                            | Ativa e desativa o salvamento de dados à tinta em copapel.                                                                          |
| HRESULT InkStart (nX curto, nY curto);                          | Inicia a sequência de desenho de tinta.                                                                                          |
| HRESULT InkDraw (nX curto, nY curto);                           | Desenha dados de sequência de tinta.                                                                                              |
| HRESULT InkStop (nX curto, nY curto);                           | Interrompe a sequência de desenho de tinta.                                                                                           |
| HRESULT ConnectPaperSink (void);                                | Conecta o objeto PaperSink do cliente à fonte de copapel do servidor.                                                    |
| HRESULT DisconnectPaperSink (void);                             | Desconecte o objeto PaperSink do cliente da fonte de copapel do servidor.                                                |
| Carga HRESULT (void);                                            | Carrega dados de tinta do arquivo composto atual.                                                                            |
| HRESULT Save (void);                                            | Salva os dados de tinta existentes no arquivo composto atual.                                                                     |
| HRESULT AskSave (void);                                         | Verifica se o desenho foi alterado. Nesse caso, exibe a caixa de diálogo solicitando que o usuário salve as alterações e responda adequadamente. |
| HRESULT Open (void);                                            | Mostra a caixa de diálogo comum do Win32. Abre o arquivo composto de dados de papel existente.                                               |
| HRESULT Saves (void);                                          | Mostra a caixa de diálogo comum do Win32. Salva os dados do papel atual no arquivo renomeado.                                              |
| COLORREF PickColor (void);                                      | Mostra a caixa de diálogo xibir do Win32. Solicita que o usuário escolha a nova cor da caneta.                                                      |



 

O método **init** cria o objeto de copapel baseado em servidor e atribui o membro pIPaper m do CGuiPaper \_ .

Os métodos **AskSave**, **Open**, **SaveAs** e **PickColor** fornecem um comportamento de GUI familiar usando caixas de diálogo comuns do Win32. Por exemplo, o método **Open** usa a caixa de diálogo Win32 Open File Name para solicitar ao usuário que especifique um nome de arquivo para abertura.

Os métodos **Load** e **Save** serão abordados em detalhes posteriormente neste Tour.

**InkSaving**, **InkStart**, **InkDraw** e **InkStop** são os métodos centrais para a funcionalidade de desenho do aplicativo **StoClien** . O **StoClien** usa esses métodos CGuiPaper para capturar, exibir e armazenar os dados de desenho interativos conforme eles ocorrem no controle do usuário. Eles executam uma função dupla de pintura da imagem desenhada para a janela do cliente, bem como a passagem dos dados de desenho para o copapel no servidor. O copaper converte os dados de desenho em pacotes de dados de tinta para armazenamento.

 

 




