---
title: Método Init – CPapFile
description: O exemplo de código a seguir mostra como CPapFile é inicializado.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- Método Init – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366490"
---
# <a name="init-method---cpapfile"></a><span data-ttu-id="f9799-104">Método Init – CPapFile</span><span class="sxs-lookup"><span data-stu-id="f9799-104">Init Method - CPapFile</span></span>

<span data-ttu-id="f9799-105">O exemplo de código a seguir mostra como **CPapFile** é inicializado.</span><span class="sxs-lookup"><span data-stu-id="f9799-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="f9799-106">Este exemplo é o método  **init** **CPapFile** de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="f9799-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



<span data-ttu-id="f9799-107">O parâmetro *pszAppFileName* é usado para inicializar CPapFile com um nome de arquivo padrão para qualquer carga subsequente ou operações de salvamento.</span><span class="sxs-lookup"><span data-stu-id="f9799-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="f9799-108">Uma cópia é mantida no membro **m \_ szCurFileName** para a primeira carga.</span><span class="sxs-lookup"><span data-stu-id="f9799-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="f9799-109">Em **StoClien**, uma carga desse tipo é tentada quando o aplicativo é iniciado pela primeira vez depois que CPapFile é inicializado com *PSZAPPFILENAME* atribuído "StoClien. PAP ".</span><span class="sxs-lookup"><span data-stu-id="f9799-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="f9799-110">Esse nome de arquivo foi construído em um Construtor CGuiPaper obtendo o nome atual do módulo em execução.</span><span class="sxs-lookup"><span data-stu-id="f9799-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="f9799-111">(A função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) do Win32 é chamada).</span><span class="sxs-lookup"><span data-stu-id="f9799-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="f9799-112">O parâmetro *pIPaper* é exigido por CPapFile, pois ele usa essa interface no objeto de copapel para executar suas operações de carregamento e salvamento.</span><span class="sxs-lookup"><span data-stu-id="f9799-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="f9799-113">**AddRef** é chamado nessa cópia armazenada de *pIPaper*, de acordo com as regras com.</span><span class="sxs-lookup"><span data-stu-id="f9799-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="f9799-114">A **versão** correspondente é chamada no destruidor CPapFile.</span><span class="sxs-lookup"><span data-stu-id="f9799-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 