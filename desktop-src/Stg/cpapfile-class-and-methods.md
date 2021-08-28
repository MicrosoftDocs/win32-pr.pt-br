---
title: Métodos e classe CPapFile
description: StoCl encapsula suas operações de arquivo composto em um objeto CPapFile C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36eaa46b9e675be2da699ed6f2fb0e2a2d8dd6db1e25cf0afba0f216f75a59e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962372"
---
# <a name="cpapfile-class-and-methods"></a>Métodos e classe CPapFile

**StoCl encapsula suas** operações de arquivo composto em um objeto CPapFile C++.

A seguir está a **declaração de classe CPapFile** de Papfile.h.


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



O objeto CPapFile mantém um nome de arquivo atual no **membro m \_ szCurFileName**. Esse nome de arquivo é usado [](save-method---cpapfile.md) como padrão nos métodos [**Carregar**](load-method---cpapfile.md) e Salvar quando eles não recebem explicitamente um nome de arquivo.

O **membro \_ m pIPaper** mantém um ponteiro de interface para a interface [**IPaper COPaper.**](ipaper-methods.md) O **membro \_ m pIStorage** mantém um ponteiro para a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para o arquivo composto atual que **o StoCl ltda** está usando para armazenamento estruturado.

A seguir está um resumo dos métodos de CPapFile.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




