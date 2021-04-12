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
# <a name="init-method---cpapfile"></a>Método Init – CPapFile

O exemplo de código a seguir mostra como **CPapFile** é inicializado.

Este exemplo é o método  **init** **CPapFile** de Papfile. cpp.


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



O parâmetro *pszAppFileName* é usado para inicializar CPapFile com um nome de arquivo padrão para qualquer carga subsequente ou operações de salvamento. Uma cópia é mantida no membro **m \_ szCurFileName** para a primeira carga. Em **StoClien**, uma carga desse tipo é tentada quando o aplicativo é iniciado pela primeira vez depois que CPapFile é inicializado com *PSZAPPFILENAME* atribuído "StoClien. PAP ". Esse nome de arquivo foi construído em um Construtor CGuiPaper obtendo o nome atual do módulo em execução. (A função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) do Win32 é chamada).

O parâmetro *pIPaper* é exigido por CPapFile, pois ele usa essa interface no objeto de copapel para executar suas operações de carregamento e salvamento. **AddRef** é chamado nessa cópia armazenada de *pIPaper*, de acordo com as regras com. A **versão** correspondente é chamada no destruidor CPapFile.

 

 