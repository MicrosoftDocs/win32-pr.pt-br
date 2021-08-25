---
title: Método Load – CPapFile
description: Quando essas operações são bem-sucedidas, a interface IStorage obtida é liberada. Isso fecha o arquivo e indica que o arquivo não é mantido aberto durante outras operações do cliente. Ele será reaberto quando necessário.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Método Load – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49eac23bcb79738a30b18eb87a4d8ef4598aba89de0748c58b433df28d614886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034886"
---
# <a name="load-method---cpapfile"></a>Método Load – CPapFile

Quando essas operações são bem-sucedidas, a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtida é liberada. Isso fecha o arquivo e indica que o arquivo não é mantido aberto durante outras operações do cliente. Ele será reaberto quando necessário.

Este exemplo é o **método CPapFile** **Load** de Papfile.cpp.


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

Assim como acontece com o método [**Save,**](save-method---cpapfile.md) se **NULL** for passado para o parâmetro *pszFileName,* o conteúdo armazenado do **membro m \_ szCurFileName** será usado para o nome do arquivo. Como um arquivo existente pode ser aberto, a função APPUTIL **FileExist** é usada primeiro para verificar se o arquivo existe. Se existir, a função de serviço [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) padrão será chamada para verificar o formato do arquivo para determinar se ele é um arquivo composto válido.

Se o arquivo for válido, a função de serviço [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) padrão será chamada para abrir o arquivo e retornar um ponteiro para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para ele.

O primeiro parâmetro é o nome do arquivo composto a ser aberto. Assim como com a [**chamada StgCreateDocfile,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) essa cadeia de caracteres é esperada no formato Unicode e, durante a compilação ANSI, uma macro APPUTIL é usada para garantir que o parâmetro ANSI seja convertido no Unicode esperado.

O segundo parâmetro de armazenamento de prioridade **é NULL,** indicando que ele não é usado neste exemplo.

Os sinalizadores de modo de acesso são passados como o terceiro parâmetro para especificar quais modos de acesso são permitidos no arquivo aberto. [**STGM \_ READ**](stgm-constants.md) abre o arquivo com permissão somente leitura. [**STGM \_ DIRECT**](stgm-constants.md) abre o arquivo para acesso direto, em vez de acesso transacionado. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.

O quarto parâmetro de exclusão de elemento **em NULL,** indicando que ele não é usado neste exemplo.

O quinto parâmetro é reservado para uso futuro e deve ser zero.

O endereço da variável de **ponteiro \_ m pIStorage** é passado como o sexto parâmetro. Quando a chamada é retornada com êxito, **m \_ pIStorage** contém um ponteiro para uma interface [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Essa é a interface usada para quaisquer operações subsequentes no arquivo aberto.

Nesse caso, a operação importante é fazer com que o objeto COPaper carregue seus dados de desenho do arquivo. Isso é feito acima usando o **método Load** da interface [**IPaper do COPaper.**](ipaper-methods.md) Se o COPaper conseguir carregar seus dados usando o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) fornecido, o nome do arquivo composto será copiado para **m \_ szCurFileName** como o novo nome de arquivo atual.

Quando essas operações são concluídas com êxito, a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtida é liberada. Isso fecha o arquivo e significa que o arquivo não é mantido aberto durante outras operações do cliente. Ele será reaberto quando necessário.

 

 




