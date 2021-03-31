---
title: Método Save – CPapFile
description: Quando CPapFile é inicializado, ele pode ser usado para salvar os dados de desenho atuais mantidos no objeto de copapel.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Método Save – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916650"
---
# <a name="save-method---cpapfile"></a>Método Save – CPapFile

Quando **CPapFile** é inicializado, ele pode ser usado para salvar os dados de desenho atuais mantidos no objeto de copapel.

## <a name="save-method-papfilecpp"></a>Método Save (PAPFILE. CPP

Este exemplo é o método **CPapFile** [**Save**](ipaper--save.md) de Papfile. cpp.


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



Se **NULL** for passado para o parâmetro *pszFileName* , o conteúdo armazenado do membro **m \_ szCurFileName** será usado para o nome do arquivo. O *nLockKey* é a chave de bloqueio do cliente obtida em uma chamada anterior para o método de [**bloqueio**](ipaper-methods.md) de copapel na interface **IPaper** .

A função de serviço [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) do com Standard é chamada para criar o arquivo composto no qual os dados de desenho serão salvos.

O nome do arquivo composto a ser criado é passado como o primeiro parâmetro. Isso é esperado por [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como uma cadeia de caracteres Unicode. Quando **StoClien** é compilado para cadeias de caracteres ANSI (Unicode não está definido, que é o padrão no Makefile), essa chamada realmente reduz para uma chamada para uma função APPUTIL interna, **um \_ StgCreateDocfile**. Essa função executa a conversão correta do parâmetro ANSI pszFile em uma versão Unicode antes de chamar **StgCreateDocfile**. Para obter mais informações, consulte Apputil. h e Stoserve.htm.

Os sinalizadores de modo de acesso são passados como o segundo parâmetro e determinam quais modos de acesso são permitidos no novo arquivo. O sinalizador [STGM \_ Create](stgm-constants.md) Access Mode cria um novo arquivo composto ou substitui um existente de mesmo nome. [STGM \_ READWRITE](stgm-constants.md) abre o arquivo com permissão de leitura/gravação. [STGM \_ DIRETO](stgm-constants.md) abre o arquivo para acesso direto, em oposição ao acesso transacionado. [STGM \_ COMPARTILHAMENTO \_ exclusivo](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.

O terceiro parâmetro é reservado e deve ser zero.

O endereço da variável de ponteiro **m \_ pIStorage** é passado para [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como o quarto parâmetro. Quando a chamada retorna com êxito, **m \_ pIStorage** contém um ponteiro de interface para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Essa é a interface que é usada para qualquer operação subsequente no arquivo.

Nesse caso, a operação importante é fazer com que o objeto de copapel armazene seus dados de desenho no arquivo. Isso é feito acima usando o método [**Save**](ipaper--save.md) da interface [**IPaper**](ipaper-methods.md) de copapel. Se o copapel tiver sucesso ao salvar seus dados no objeto de armazenamento fornecido, o nome do arquivo composto será copiado em **m \_ szCurFileName** como o novo nome de arquivo atual.

 

 




