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
# <a name="load-method---cpapfile"></a><span data-ttu-id="b222b-106">Método de carregamento-CPapFile</span><span class="sxs-lookup"><span data-stu-id="b222b-106">Load Method - CPapFile</span></span>

<span data-ttu-id="b222b-107">Quando essas operações são bem-sucedidas, a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtida é liberada.</span><span class="sxs-lookup"><span data-stu-id="b222b-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="b222b-108">Isso fecha o arquivo e indica que o arquivo não é mantido aberto durante outras operações do cliente.</span><span class="sxs-lookup"><span data-stu-id="b222b-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="b222b-109">Ele será reaberto quando necessário.</span><span class="sxs-lookup"><span data-stu-id="b222b-109">It will be reopened when required.</span></span>

<span data-ttu-id="b222b-110">Este exemplo é o método de  **carregamento** **CPapFile** de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="b222b-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


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



### <a name="remarks"></a><span data-ttu-id="b222b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b222b-111">Remarks</span></span>

<span data-ttu-id="b222b-112">Assim como acontece com o método [**Save**](save-method---cpapfile.md) , se **NULL** for passado para o parâmetro *pszFileName* , o conteúdo armazenado do membro **m \_ szCurFileName** será usado para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b222b-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="b222b-113">Como um arquivo existente pode ser aberto, a função **FileExist** APPUTIL é usada primeiro para verificar se o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="b222b-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="b222b-114">Se existir, a função de serviço [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) padrão será chamada para verificar o formato do arquivo para determinar se ele é um arquivo composto válido.</span><span class="sxs-lookup"><span data-stu-id="b222b-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="b222b-115">Se o arquivo for válido, a função de serviço [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) padrão será chamada para abrir o arquivo e retornar um ponteiro para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para ele.</span><span class="sxs-lookup"><span data-stu-id="b222b-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="b222b-116">O primeiro parâmetro é o nome do arquivo composto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="b222b-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="b222b-117">Assim como acontece com a chamada [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , essa cadeia de caracteres é esperada no formato Unicode e, durante a compilação ANSI, uma macro APPUTIL é usada para garantir que o parâmetro ANSI seja convertido para o Unicode esperado.</span><span class="sxs-lookup"><span data-stu-id="b222b-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="b222b-118">O segundo parâmetro de armazenamento de prioridade é **nulo**, indicando que ele não é usado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="b222b-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="b222b-119">Os sinalizadores de modo de acesso são passados como o terceiro parâmetro para especificar quais modos de acesso são permitidos no arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="b222b-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="b222b-120">[**STGM \_ LER**](stgm-constants.md) abre o arquivo com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b222b-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="b222b-121">[**STGM \_ DIRETO**](stgm-constants.md) abre o arquivo para acesso direto, em oposição ao acesso transacionado.</span><span class="sxs-lookup"><span data-stu-id="b222b-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="b222b-122">[**STGM \_ COMPARTILHAMENTO \_ exclusivo**](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="b222b-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="b222b-123">O quarto parâmetro de exclusão de elemento em **NULL**, indicando que ele não é usado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="b222b-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="b222b-124">O quinto parâmetro é reservado para uso futuro e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b222b-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="b222b-125">O endereço da variável de ponteiro **m \_ pIStorage** é passado como o sexto parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b222b-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="b222b-126">Quando a chamada retorna com êxito, **m \_ pIStorage** contém um ponteiro para uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="b222b-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="b222b-127">Essa é a interface usada para qualquer operação subsequente no arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="b222b-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="b222b-128">Nesse caso, a operação importante é fazer com que o objeto de copapel carregue seus dados de desenho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b222b-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="b222b-129">Isso é feito acima usando o método **Load** da interface [**IPaper**](ipaper-methods.md) do copaper.</span><span class="sxs-lookup"><span data-stu-id="b222b-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="b222b-130">Se o copapel tiver sucesso ao carregar seus dados usando o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) fornecido, o nome do arquivo composto será copiado em **m \_ szCurFileName** como o novo nome de arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="b222b-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="b222b-131">Quando essas operações são concluídas com êxito, a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtida é liberada.</span><span class="sxs-lookup"><span data-stu-id="b222b-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="b222b-132">Isso fecha o arquivo e significa que o arquivo não é mantido aberto durante outras operações do cliente.</span><span class="sxs-lookup"><span data-stu-id="b222b-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="b222b-133">Ele será reaberto quando necessário.</span><span class="sxs-lookup"><span data-stu-id="b222b-133">It will be reopened when required.</span></span>

 

 




