---
title: Classe e métodos CPapFile
description: StoClien encapsula suas operações de arquivo composto em um objeto CPapFile C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916146"
---
# <a name="cpapfile-class-and-methods"></a>Classe e métodos CPapFile

**StoClien** encapsula suas operações de arquivo composto em um objeto CPapFile C++.

A seguir está a declaração de classe **CPapFile** de Papfile. h.


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



O objeto CPapFile mantém um nome de arquivo atual no membro **m \_ szCurFileName**. Esse nome de arquivo é usado como padrão nos métodos [**Load**](load-method---cpapfile.md) e [**Save**](save-method---cpapfile.md) quando eles não recebem explicitamente um nome de arquivo.

O membro **m \_ pIPaper** mantém um ponteiro de interface para a interface [**IPaper**](ipaper-methods.md) de copapel. O membro **m \_ pIStorage** mantém um ponteiro para a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para o arquivo composto atual que o **StoClien** está usando para o armazenamento estruturado.

Veja a seguir um resumo dos métodos do CPapFile.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




