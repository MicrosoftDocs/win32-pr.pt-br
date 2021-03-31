---
title: Declaração de classe CGuiPaper
description: Declaração de classe CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005049"
---
# <a name="cguipaper-class-declaration"></a>Declaração de classe CGuiPaper

A seguir está a declaração de classe **CGuiPaper** de GUIPAPER. H.


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



**CGuiPaper** mantém as propriedades de GUI atuais para o papel de desenho. Os membros **m \_ crInkColor**, **m \_ crInkWidth** e **m \_ WinRect** contêm valores para a cor da tinta atual, a largura da tinta e o retângulo do desenho. O **membro \_ HWND do m** armazena o identificador para a janela em que a pintura é feita.

A pintura real de imagens é feita usando um identificador para um contexto de dispositivo mantido no membro **m \_ HDC**. Um identificador para a caneta de desenho atual é mantido no membro **m \_ hPen**. A caneta é destruída e recriada quando sua cor ou largura é alterada pelo usuário.

Os membros **m \_ pCOPaperSink** e **m \_ dwPaperSink** contêm valores necessários para a conexão com o copaper para receber notificações de entrada por meio da interface [**IPaperSink**](ipapersink-methods.md) . O membro **m \_ bDirty** contém um sinalizador que indica que o usuário alterou o desenho e que ele não reflete mais os dados armazenados em seu arquivo.

O membro **m \_ pIPaper** mantém o ponteiro da interface principal para o objeto de copapel. Toda a funcionalidade de copapel é acessada por meio desse ponteiro.

O membro **m \_ nLockKey** é usado para dar suporte a um esquema de bloqueio de cliente que é usado com vários clientes para permitir que um cliente tenha acesso exclusivo a um objeto de copapel compartilhado. O copaper atribui **m \_ nLockKey** durante uma chamada [**IPaper**](ipaper-methods.md)::**Lock** e é passado como um parâmetro pelo cliente em chamadas subsequentes para o copaper. O copaper executará o trabalho nessas chamadas somente se a chave de bloqueio passada corresponder à chave do último entregue a um cliente por copaper.

O membro **m \_ pPapFile** mantém um ponteiro para um objeto [**CPapFile**](cpapfile-class-and-methods.md) . É um objeto C++ que encapsula operações de carregamento e salvamento em um arquivo composto de armazenamento estruturado. O **CPapFile** trabalha com o objeto de copapel subjacente baseado em servidor para carregar e salvar os dados de desenho de copapel.

 

 




