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
# <a name="save-method---cpapfile"></a><span data-ttu-id="7c068-104">Método Save – CPapFile</span><span class="sxs-lookup"><span data-stu-id="7c068-104">Save Method - CPapFile</span></span>

<span data-ttu-id="7c068-105">Quando **CPapFile** é inicializado, ele pode ser usado para salvar os dados de desenho atuais mantidos no objeto de copapel.</span><span class="sxs-lookup"><span data-stu-id="7c068-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="7c068-106">Método Save (PAPFILE. CPP</span><span class="sxs-lookup"><span data-stu-id="7c068-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="7c068-107">Este exemplo é o método **CPapFile** [**Save**](ipaper--save.md) de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="7c068-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


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



<span data-ttu-id="7c068-108">Se **NULL** for passado para o parâmetro *pszFileName* , o conteúdo armazenado do membro **m \_ szCurFileName** será usado para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c068-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="7c068-109">O *nLockKey* é a chave de bloqueio do cliente obtida em uma chamada anterior para o método de [**bloqueio**](ipaper-methods.md) de copapel na interface **IPaper** .</span><span class="sxs-lookup"><span data-stu-id="7c068-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="7c068-110">A função de serviço [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) do com Standard é chamada para criar o arquivo composto no qual os dados de desenho serão salvos.</span><span class="sxs-lookup"><span data-stu-id="7c068-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="7c068-111">O nome do arquivo composto a ser criado é passado como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7c068-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="7c068-112">Isso é esperado por [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="7c068-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="7c068-113">Quando **StoClien** é compilado para cadeias de caracteres ANSI (Unicode não está definido, que é o padrão no Makefile), essa chamada realmente reduz para uma chamada para uma função APPUTIL interna, **um \_ StgCreateDocfile**.</span><span class="sxs-lookup"><span data-stu-id="7c068-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="7c068-114">Essa função executa a conversão correta do parâmetro ANSI pszFile em uma versão Unicode antes de chamar **StgCreateDocfile**.</span><span class="sxs-lookup"><span data-stu-id="7c068-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="7c068-115">Para obter mais informações, consulte Apputil. h e Stoserve.htm.</span><span class="sxs-lookup"><span data-stu-id="7c068-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="7c068-116">Os sinalizadores de modo de acesso são passados como o segundo parâmetro e determinam quais modos de acesso são permitidos no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c068-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="7c068-117">O sinalizador [STGM \_ Create](stgm-constants.md) Access Mode cria um novo arquivo composto ou substitui um existente de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="7c068-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="7c068-118">[STGM \_ READWRITE](stgm-constants.md) abre o arquivo com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7c068-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="7c068-119">[STGM \_ DIRETO](stgm-constants.md) abre o arquivo para acesso direto, em oposição ao acesso transacionado.</span><span class="sxs-lookup"><span data-stu-id="7c068-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="7c068-120">[STGM \_ COMPARTILHAMENTO \_ exclusivo](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="7c068-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="7c068-121">O terceiro parâmetro é reservado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7c068-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="7c068-122">O endereço da variável de ponteiro **m \_ pIStorage** é passado para [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como o quarto parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7c068-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="7c068-123">Quando a chamada retorna com êxito, **m \_ pIStorage** contém um ponteiro de interface para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="7c068-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="7c068-124">Essa é a interface que é usada para qualquer operação subsequente no arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c068-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="7c068-125">Nesse caso, a operação importante é fazer com que o objeto de copapel armazene seus dados de desenho no arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c068-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="7c068-126">Isso é feito acima usando o método [**Save**](ipaper--save.md) da interface [**IPaper**](ipaper-methods.md) de copapel.</span><span class="sxs-lookup"><span data-stu-id="7c068-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="7c068-127">Se o copapel tiver sucesso ao salvar seus dados no objeto de armazenamento fornecido, o nome do arquivo composto será copiado em **m \_ szCurFileName** como o novo nome de arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="7c068-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




