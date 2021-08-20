---
title: Método Save – CPapFile
description: Quando CPapFile é inicializado, ele pode ser usado para salvar os dados de desenho atuais mantidos no objeto COPaper.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Método Save – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b465d5b275949b3cdfcea04a5023cd110a8600c59a706d2c2f1515e4225c757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960593"
---
# <a name="save-method---cpapfile"></a>Método Save – CPapFile

Quando **CPapFile** é inicializado, ele pode ser usado para salvar os dados de desenho atuais mantidos no objeto COPaper.

## <a name="save-method-papfilecpp"></a>Método Save (PAPFILE. CPP)

Este exemplo é o **método CPapFile** [**Save**](ipaper--save.md) de Papfile.cpp.


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



Se **NULL** for passado para o *parâmetro pszFileName,* o conteúdo armazenado do **membro m \_ szCurFileName** será usado para o nome do arquivo. O *nLockKey* é a chave de bloqueio do cliente obtida em uma chamada anterior para o método COPaper [**Lock**](ipaper-methods.md) na interface **IPaper.**

A função de [**serviço StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) padrão COM é chamada para criar o arquivo composto no qual os dados de desenho serão salvos.

O nome do arquivo composto a ser criado é passado como o primeiro parâmetro. Isso é esperado por [**StgCreateDocfile como**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) uma cadeia de caracteres Unicode. Quando **StoCl ltda** é compilado para cadeias de caracteres ANSI (UNICODE não está definido, que é o padrão no makefile), essa chamada realmente reduz para uma chamada para uma função APPUTIL interna, **Um \_ StgCreateDocfile**. Essa função executa a conversão adequada do parâmetro anSI pszFile em uma versão Unicode antes de **chamar StgCreateDocfile**. Para obter mais informações, consulte Apputil.h e Stoserve.htm.

Os sinalizadores de modo de acesso são passados como o segundo parâmetro e determinam quais modos de acesso são permitidos no novo arquivo. O sinalizador de modo de [ \_ acesso STGM CREATE](stgm-constants.md) cria um novo arquivo composto ou substitui um existente com o mesmo nome. [STGM \_ READWRITE](stgm-constants.md) abre o arquivo com permissão de leitura/gravação. [STGM \_ DIRECT](stgm-constants.md) abre o arquivo para acesso direto, em vez de acesso transacionado. [STGM \_ SHARE \_ EXCLUSIVE](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.

O terceiro parâmetro é reservado e deve ser zero.

O endereço da variável de **ponteiro \_ m pIStorage** é passado [**para StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como o quarto parâmetro. Quando a chamada é retornada com êxito, **m \_ pIStorage** contém um ponteiro de interface para uma interface [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Essa é a interface usada para quaisquer operações subsequentes no arquivo.

Nesse caso, a operação importante é fazer com que o objeto COPaper armazene seus dados de desenho no arquivo. Isso é feito acima usando o [**método Save**](ipaper--save.md) da interface [**IPaper COPaper.**](ipaper-methods.md) Se o COPaper tiver êxito ao salvar seus dados no objeto de armazenamento fornecido, o nome do arquivo composto será copiado para **m \_ szCurFileName** como o novo nome de arquivo atual.

 

 




