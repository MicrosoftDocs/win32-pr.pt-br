---
title: Adicionando arquivos a um trabalho
description: Um trabalho contém um ou mais arquivos que você deseja transferir.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- transferir BITS de trabalho, adicionando arquivos
- BITS de transferência de arquivo, adicionando
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: b6c369c0a9ee207790d0370da6543c642ee294b072e0d91f1837cd734a6a625d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529266"
---
# <a name="adding-files-to-a-job"></a>Adicionando arquivos a um trabalho

Um trabalho contém um ou mais arquivos que você deseja transferir. Use um dos seguintes métodos para adicionar arquivos a um trabalho:

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Adiciona um único arquivo a um trabalho.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Método ibackgroundcopyjob:: addfileset**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Adiciona um ou mais arquivos a um trabalho. Se você estiver adicionando vários arquivos, será mais eficiente chamar esse método do que chamar o método **AddFile** em um loop.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Adiciona um único arquivo a um trabalho. Use esse método se desejar baixar intervalos de dados de um arquivo. Você pode usar esse método somente para baixar trabalhos.

</dd> </dl>

Ao adicionar um arquivo a um trabalho, você especifica o nome remoto e o nome local do arquivo. Para obter detalhes sobre o formato dos nomes de arquivo local e remoto, consulte a estrutura de [**\_ \_ informações de arquivo BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .

Um trabalho de carregamento pode conter apenas um arquivo. Os métodos [**método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) e [**método ibackgroundcopyjob:: addfileset**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) retornam \_ BG \_ E \_ muitos \_ arquivos se você tentar adicionar mais de um arquivo a um trabalho de carregamento. Se você precisar carregar mais de um arquivo, considere usar um arquivo CAB ou ZIP.

Para trabalhos de download, o BITS limita o número de arquivos que um usuário pode adicionar a um trabalho para 200 arquivos e o número de intervalos de um arquivo para 500 intervalos. Esses limites não se aplicam a administradores ou serviços. Para alterar esses limites padrão, consulte [políticas de grupo](group-policies.md).

O proprietário do trabalho ou um usuário com privilégios de administrador pode adicionar arquivos ao trabalho a qualquer momento antes de chamar o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .

Se precisar alterar o nome remoto do arquivo depois de adicionar o arquivo ao trabalho, você poderá chamar o método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou o método [**IBackgroundCopyFile2:: setremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) . Use o método **ReplaceRemotePrefix** para alterar a parte do servidor do nome remoto quando o servidor não estiver disponível ou para permitir que os usuários móveis se conectem ao servidor mais próximo. Use o método **Setremotename** para alterar o protocolo usado para transferir o arquivo ou para alterar o nome ou o caminho do arquivo.

O BITS cria um arquivo temporário no diretório de destino e usa o arquivo temporário para a transferência de arquivo. Para obter o nome de arquivo temporário, chame o método [**IBackgroundCopyFile3:: Gettemporárioname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) . O BITS altera o nome do arquivo temporário para o nome do arquivo de destino quando você chama o método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . O BITS não especifica um descritor de segurança quando ele [**cria**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o arquivo temporário (o arquivo herda as informações de ACL do diretório de destino). Se os dados transferidos forem confidenciais, o aplicativo deverá especificar uma ACL apropriada no diretório de destino para impedir o acesso não autorizado.

Para manter as informações de proprietário e ACL com o arquivo transferido, chame o método [**IBackgroundCopyJob3:: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .

O proprietário do trabalho (o usuário que criou o trabalho ou o administrador que [assumiu a propriedade](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) do trabalho) deve ter permissões para o arquivo no servidor, bem como o cliente. Por exemplo, para baixar um arquivo, o usuário deve ter permissões de leitura no servidor e permissões de gravação para o diretório local no cliente.

O exemplo a seguir mostra como adicionar um único arquivo ao trabalho. O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, é válido.


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



O exemplo a seguir mostra como adicionar vários arquivos ao trabalho. O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, é válido e os nomes local e remoto são provenientes de uma lista na interface do usuário.


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



 

 