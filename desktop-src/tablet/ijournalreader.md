---
description: Fornece acesso de leitura a um arquivo de diário do Windows, retornando um fluxo que contém uma versão XML do conteúdo do arquivo.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interface IJournalReader (Journal. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297631"
---
# <a name="ijournalreader-interface"></a><span data-ttu-id="62795-103">Interface IJournalReader</span><span class="sxs-lookup"><span data-stu-id="62795-103">IJournalReader interface</span></span>

<span data-ttu-id="62795-104">Fornece acesso de leitura a um arquivo de diário do Windows, retornando um fluxo que contém uma versão XML do conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="62795-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="62795-105">O componente de leitor de diário não pode ler arquivos de diário do Windows criados por computadores que executam o Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="62795-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="62795-106">A interface IJournalReader deve ser considerada preterida ou obsoleta e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="62795-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="62795-107">Membros</span><span class="sxs-lookup"><span data-stu-id="62795-107">Members</span></span>

<span data-ttu-id="62795-108">A interface **IJournalReader** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="62795-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62795-109">**IJournalReader** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="62795-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="62795-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="62795-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62795-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="62795-111">Methods</span></span>

<span data-ttu-id="62795-112">A interface **IJournalReader** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="62795-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="62795-113">Método</span><span class="sxs-lookup"><span data-stu-id="62795-113">Method</span></span>                                                  | <span data-ttu-id="62795-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="62795-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62795-115">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="62795-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="62795-116">Usa um fluxo para um arquivo de anotação do diário e retorna um fluxo XML que representa o conteúdo do documento.</span><span class="sxs-lookup"><span data-stu-id="62795-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62795-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="62795-117">Remarks</span></span>

<span data-ttu-id="62795-118">A classe **JournalReader** permite carregar um fluxo de documento de diário e receber um fluxo XML que representa o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="62795-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="62795-119">Você pode reconstituir, exibir e manipular a tinta.</span><span class="sxs-lookup"><span data-stu-id="62795-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="62795-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62795-120">Examples</span></span>

<span data-ttu-id="62795-121">O exemplo a seguir de um manipulador para o evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de um botão cria uma instância da classe **JournalReader** e a usa para ler um arquivo de diário existente.</span><span class="sxs-lookup"><span data-stu-id="62795-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="62795-122">O método **DisplayXml** chamado a partir deste exemplo não é mostrado.</span><span class="sxs-lookup"><span data-stu-id="62795-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="62795-123">A implementação específica desse método é dependente das necessidades do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="62795-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a><span data-ttu-id="62795-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62795-124">Requirements</span></span>



| <span data-ttu-id="62795-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62795-125">Requirement</span></span> | <span data-ttu-id="62795-126">Valor</span><span class="sxs-lookup"><span data-stu-id="62795-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62795-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62795-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62795-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="62795-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62795-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62795-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62795-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62795-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="62795-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62795-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="62795-132"><dt>Journal. h (também requer Journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="62795-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="62795-133">DLL</span><span class="sxs-lookup"><span data-stu-id="62795-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62795-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62795-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="62795-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="62795-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62795-136">GUIDs de propriedade personalizada</span><span class="sxs-lookup"><span data-stu-id="62795-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="62795-137">**Método ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="62795-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

