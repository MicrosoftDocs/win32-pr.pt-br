---
title: Declaração de classe CGuiPaper
description: Declaração de classe CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d684618eea78247b94ed03223cfce45d2cc713f5507b1e290731d3451212b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663516"
---
# <a name="cguipaper-class-declaration"></a>Declaração de classe CGuiPaper

A seguir está a declaração de classe **CGuiPaper** de GUIPAPER.H.


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



**O CGuiPaper** mantém as propriedades de GUI atuais para o papel de desenho. Os **membros m \_ crInkColor**, **m \_ crInkWidth** e **m \_ WinRect** contêm valores para a cor de tinta atual, a largura da tinta e o retângulo de desenho. O **membro \_ m hWnd** armazena a alça na janela em que a pintura é feita.

A pintura real de imagens é feita usando uma alça para um contexto de dispositivo mantido no **membro m \_ hDC.** Um alça para a caneta de desenho atual é mantido no **membro m \_ hPen**. A caneta é destruída e recriada quando sua cor ou largura é alterada pelo usuário.

Membros **m \_ pCOPaperSink** e **m \_ dwPaperSink** retivem os valores necessários para se conectar ao COPaper para receber notificações de entrada por meio da interface [**IPaperSink.**](ipapersink-methods.md) O **membro \_ m bDirty** contém um sinalizador que indica que o usuário alterou o desenho e que ele não reflete mais os dados armazenados em seu arquivo.

O **membro \_ m pIPaper** contém o ponteiro da interface principal para o objeto COPaper. Toda a funcionalidade COPaper é acessada por meio desse ponteiro.

O **membro \_ m nLockKey** é usado para dar suporte a um esquema de bloqueio de cliente que é usado com vários clientes para permitir que um cliente tenha acesso exclusivo a um objeto COPaper compartilhado. O COPaper atribui **m \_ nLockKey** durante uma chamada [**IPaper**](ipaper-methods.md)::**Lock** e é passado como um parâmetro pelo cliente em chamadas subsequentes para COPaper. O COPaper executará o trabalho nessas chamadas somente se a chave de bloqueio passada corresponde à chave entregue pela última vez a um cliente pelo COPaper.

O **membro \_ m pPapFile** contém um ponteiro para um [**objeto CPapFile.**](cpapfile-class-and-methods.md) É um objeto C++ que encapsula operações de carregamento e de salvar em um arquivo composto de armazenamento estruturado. **O CPapFile** funciona com o objeto COPaper baseado em servidor subjacente para carregar e salvar os dados de desenho do COPaper.

 

 




