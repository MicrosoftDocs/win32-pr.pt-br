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
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="a5987-103">Declaração de classe CGuiPaper</span><span class="sxs-lookup"><span data-stu-id="a5987-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="a5987-104">A seguir está a declaração de classe **CGuiPaper** de GUIPAPER. H.</span><span class="sxs-lookup"><span data-stu-id="a5987-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


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



<span data-ttu-id="a5987-105">**CGuiPaper** mantém as propriedades de GUI atuais para o papel de desenho.</span><span class="sxs-lookup"><span data-stu-id="a5987-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="a5987-106">Os membros **m \_ crInkColor**, **m \_ crInkWidth** e **m \_ WinRect** contêm valores para a cor da tinta atual, a largura da tinta e o retângulo do desenho.</span><span class="sxs-lookup"><span data-stu-id="a5987-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="a5987-107">O **membro \_ HWND do m** armazena o identificador para a janela em que a pintura é feita.</span><span class="sxs-lookup"><span data-stu-id="a5987-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="a5987-108">A pintura real de imagens é feita usando um identificador para um contexto de dispositivo mantido no membro **m \_ HDC**.</span><span class="sxs-lookup"><span data-stu-id="a5987-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="a5987-109">Um identificador para a caneta de desenho atual é mantido no membro **m \_ hPen**.</span><span class="sxs-lookup"><span data-stu-id="a5987-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="a5987-110">A caneta é destruída e recriada quando sua cor ou largura é alterada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a5987-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="a5987-111">Os membros **m \_ pCOPaperSink** e **m \_ dwPaperSink** contêm valores necessários para a conexão com o copaper para receber notificações de entrada por meio da interface [**IPaperSink**](ipapersink-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="a5987-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="a5987-112">O membro **m \_ bDirty** contém um sinalizador que indica que o usuário alterou o desenho e que ele não reflete mais os dados armazenados em seu arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5987-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="a5987-113">O membro **m \_ pIPaper** mantém o ponteiro da interface principal para o objeto de copapel.</span><span class="sxs-lookup"><span data-stu-id="a5987-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="a5987-114">Toda a funcionalidade de copapel é acessada por meio desse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a5987-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="a5987-115">O membro **m \_ nLockKey** é usado para dar suporte a um esquema de bloqueio de cliente que é usado com vários clientes para permitir que um cliente tenha acesso exclusivo a um objeto de copapel compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a5987-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="a5987-116">O copaper atribui **m \_ nLockKey** durante uma chamada [**IPaper**](ipaper-methods.md)::**Lock** e é passado como um parâmetro pelo cliente em chamadas subsequentes para o copaper.</span><span class="sxs-lookup"><span data-stu-id="a5987-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="a5987-117">O copaper executará o trabalho nessas chamadas somente se a chave de bloqueio passada corresponder à chave do último entregue a um cliente por copaper.</span><span class="sxs-lookup"><span data-stu-id="a5987-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="a5987-118">O membro **m \_ pPapFile** mantém um ponteiro para um objeto [**CPapFile**](cpapfile-class-and-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="a5987-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="a5987-119">É um objeto C++ que encapsula operações de carregamento e salvamento em um arquivo composto de armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="a5987-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="a5987-120">O **CPapFile** trabalha com o objeto de copapel subjacente baseado em servidor para carregar e salvar os dados de desenho de copapel.</span><span class="sxs-lookup"><span data-stu-id="a5987-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




