---
title: Método de carregamento-CPapFile
description: Quando essas operações são bem-sucedidas, a interface IStorage obtida é liberada. Isso fecha o arquivo e indica que o arquivo não é mantido aberto durante outras operações do cliente. Ele será reaberto quando necessário.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Método de carregamento-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823062"
---
# <a name="load-method---cpapfile"></a>Método de carregamento-CPapFile

Quando essas operações são bem-sucedidas, a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtida é liberada. Isso fecha o arquivo e indica que o arquivo não é mantido aberto durante outras operações do cliente. Ele será reaberto quando necessário.

Este exemplo é o método de  **carregamento** **CPapFile** de Papfile. cpp.


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a>Comentários

Assim como acontece com o método [**Save**](save-method---cpapfile.md) , se **NULL** for passado para o parâmetro *pszFileName* , o conteúdo armazenado do membro **m \_ szCurFileName** será usado para o nome do arquivo. Como um arquivo existente pode ser aberto, a função **FileExist** APPUTIL é usada primeiro para verificar se o arquivo existe. Se existir, a função de serviço [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) padrão será chamada para verificar o formato do arquivo para determinar se ele é um arquivo composto válido.

Se o arquivo for válido, a função de serviço [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) padrão será chamada para abrir o arquivo e retornar um ponteiro para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para ele.

O primeiro parâmetro é o nome do arquivo composto a ser aberto. Assim como acontece com a chamada [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , essa cadeia de caracteres é esperada no formato Unicode e, durante a compilação ANSI, uma macro APPUTIL é usada para garantir que o parâmetro ANSI seja convertido para o Unicode esperado.

O segundo parâmetro de armazenamento de prioridade é **nulo**, indicando que ele não é usado neste exemplo.

Os sinalizadores de modo de acesso são passados como o terceiro parâmetro para especificar quais modos de acesso são permitidos no arquivo aberto. [**STGM \_ LER**](stgm-constants.md) abre o arquivo com permissão somente leitura. [**STGM \_ DIRETO**](stgm-constants.md) abre o arquivo para acesso direto, em oposição ao acesso transacionado. [**STGM \_ COMPARTILHAMENTO \_ exclusivo**](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.

O quarto parâmetro de exclusão de elemento em **NULL**, indicando que ele não é usado neste exemplo.

O quinto parâmetro é reservado para uso futuro e deve ser zero.

O endereço da variável de ponteiro **m \_ pIStorage** é passado como o sexto parâmetro. Quando a chamada retorna com êxito, **m \_ pIStorage** contém um ponteiro para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Essa é a interface usada para qualquer operação subsequente no arquivo aberto.

Nesse caso, a operação importante é fazer com que o objeto de copapel carregue seus dados de desenho do arquivo. Isso é feito acima usando o método **Load** da interface [**IPaper**](ipaper-methods.md) do copaper. Se o copapel tiver sucesso ao carregar seus dados usando o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) fornecido, o nome do arquivo composto será copiado em **m \_ szCurFileName** como o novo nome de arquivo atual.

Quando essas operações são concluídas com êxito, a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtida é liberada. Isso fecha o arquivo e significa que o arquivo não é mantido aberto durante outras operações do cliente. Ele será reaberto quando necessário.

 

 




