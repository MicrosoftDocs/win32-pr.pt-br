---
title: Adicionando arquivos a um trabalho
description: Um trabalho contém um ou mais arquivos que você deseja transferir.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- transferir BITS de trabalho, adicionando arquivos
- BITS de transferência de arquivo, adicionando
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917447"
---
# <a name="adding-files-to-a-job"></a><span data-ttu-id="163df-105">Adicionando arquivos a um trabalho</span><span class="sxs-lookup"><span data-stu-id="163df-105">Adding Files to a Job</span></span>

<span data-ttu-id="163df-106">Um trabalho contém um ou mais arquivos que você deseja transferir.</span><span class="sxs-lookup"><span data-stu-id="163df-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="163df-107">Use um dos seguintes métodos para adicionar arquivos a um trabalho:</span><span class="sxs-lookup"><span data-stu-id="163df-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="163df-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="163df-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="163df-109">Adiciona um único arquivo a um trabalho.</span><span class="sxs-lookup"><span data-stu-id="163df-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="163df-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Método ibackgroundcopyjob:: addfileset**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="163df-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="163df-111">Adiciona um ou mais arquivos a um trabalho.</span><span class="sxs-lookup"><span data-stu-id="163df-111">Adds one or more files to a job.</span></span> <span data-ttu-id="163df-112">Se você estiver adicionando vários arquivos, será mais eficiente chamar esse método do que chamar o método **AddFile** em um loop.</span><span class="sxs-lookup"><span data-stu-id="163df-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="163df-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="163df-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="163df-114">Adiciona um único arquivo a um trabalho.</span><span class="sxs-lookup"><span data-stu-id="163df-114">Adds a single file to a job.</span></span> <span data-ttu-id="163df-115">Use esse método se desejar baixar intervalos de dados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="163df-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="163df-116">Você pode usar esse método somente para baixar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="163df-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="163df-117">Ao adicionar um arquivo a um trabalho, você especifica o nome remoto e o nome local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="163df-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="163df-118">Para obter detalhes sobre o formato dos nomes de arquivo local e remoto, consulte a estrutura de [**\_ \_ informações de arquivo BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .</span><span class="sxs-lookup"><span data-stu-id="163df-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="163df-119">Um trabalho de carregamento pode conter apenas um arquivo.</span><span class="sxs-lookup"><span data-stu-id="163df-119">An upload job can contain only one file.</span></span> <span data-ttu-id="163df-120">Os métodos [**método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) e [**método ibackgroundcopyjob:: addfileset**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) retornam \_ BG \_ E \_ muitos \_ arquivos se você tentar adicionar mais de um arquivo a um trabalho de carregamento.</span><span class="sxs-lookup"><span data-stu-id="163df-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="163df-121">Se você precisar carregar mais de um arquivo, considere usar um arquivo CAB ou ZIP.</span><span class="sxs-lookup"><span data-stu-id="163df-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="163df-122">Para trabalhos de download, o BITS limita o número de arquivos que um usuário pode adicionar a um trabalho para 200 arquivos e o número de intervalos de um arquivo para 500 intervalos.</span><span class="sxs-lookup"><span data-stu-id="163df-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="163df-123">Esses limites não se aplicam a administradores ou serviços.</span><span class="sxs-lookup"><span data-stu-id="163df-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="163df-124">Para alterar esses limites padrão, consulte [políticas de grupo](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="163df-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="163df-125">O proprietário do trabalho ou um usuário com privilégios de administrador pode adicionar arquivos ao trabalho a qualquer momento antes de chamar o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="163df-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="163df-126">Se precisar alterar o nome remoto do arquivo depois de adicionar o arquivo ao trabalho, você poderá chamar o método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou o método [**IBackgroundCopyFile2:: setremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) .</span><span class="sxs-lookup"><span data-stu-id="163df-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="163df-127">Use o método **ReplaceRemotePrefix** para alterar a parte do servidor do nome remoto quando o servidor não estiver disponível ou para permitir que os usuários móveis se conectem ao servidor mais próximo.</span><span class="sxs-lookup"><span data-stu-id="163df-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="163df-128">Use o método **Setremotename** para alterar o protocolo usado para transferir o arquivo ou para alterar o nome ou o caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="163df-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="163df-129">O BITS cria um arquivo temporário no diretório de destino e usa o arquivo temporário para a transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="163df-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="163df-130">Para obter o nome de arquivo temporário, chame o método [**IBackgroundCopyFile3:: Gettemporárioname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) .</span><span class="sxs-lookup"><span data-stu-id="163df-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="163df-131">O BITS altera o nome do arquivo temporário para o nome do arquivo de destino quando você chama o método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="163df-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="163df-132">O BITS não especifica um descritor de segurança quando ele [**cria**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o arquivo temporário (o arquivo herda as informações de ACL do diretório de destino).</span><span class="sxs-lookup"><span data-stu-id="163df-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="163df-133">Se os dados transferidos forem confidenciais, o aplicativo deverá especificar uma ACL apropriada no diretório de destino para impedir o acesso não autorizado.</span><span class="sxs-lookup"><span data-stu-id="163df-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="163df-134">Para manter as informações de proprietário e ACL com o arquivo transferido, chame o método [**IBackgroundCopyJob3:: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .</span><span class="sxs-lookup"><span data-stu-id="163df-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="163df-135">O proprietário do trabalho (o usuário que criou o trabalho ou o administrador que [assumiu a propriedade](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) do trabalho) deve ter permissões para o arquivo no servidor, bem como o cliente.</span><span class="sxs-lookup"><span data-stu-id="163df-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="163df-136">Por exemplo, para baixar um arquivo, o usuário deve ter permissões de leitura no servidor e permissões de gravação para o diretório local no cliente.</span><span class="sxs-lookup"><span data-stu-id="163df-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="163df-137">O exemplo a seguir mostra como adicionar um único arquivo ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="163df-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="163df-138">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, é válido.</span><span class="sxs-lookup"><span data-stu-id="163df-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



<span data-ttu-id="163df-139">O exemplo a seguir mostra como adicionar vários arquivos ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="163df-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="163df-140">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, é válido e os nomes local e remoto são provenientes de uma lista na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="163df-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 