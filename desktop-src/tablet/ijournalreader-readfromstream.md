---
description: Usa um fluxo para um arquivo de anotação do diário e retorna um fluxo XML que representa o conteúdo do documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'Método IJournalReader:: ReadFromStream (Journal. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761220"
---
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="bc86c-103">Método IJournalReader:: ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="bc86c-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="bc86c-104">Usa um fluxo para um arquivo de anotação do diário e retorna um fluxo XML que representa o conteúdo do documento.</span><span class="sxs-lookup"><span data-stu-id="bc86c-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="bc86c-105">O componente de leitor de diário não pode ler arquivos de diário do Windows criados por computadores que executam o Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bc86c-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="bc86c-106">A interface IJournalReader deve ser considerada preterida ou obsoleta e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="bc86c-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bc86c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc86c-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="bc86c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc86c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc86c-109">*pJournalFileStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc86c-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc86c-110">Um objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que representa o arquivo de diário a ser lido.</span><span class="sxs-lookup"><span data-stu-id="bc86c-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="bc86c-111">*ppXmlStream* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bc86c-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bc86c-112">Um ponteiro para o endereço de um objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que receberá o fluxo XML criado lendo o arquivo de diário.</span><span class="sxs-lookup"><span data-stu-id="bc86c-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc86c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc86c-113">Return value</span></span>

<span data-ttu-id="bc86c-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc86c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc86c-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc86c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc86c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc86c-116">Remarks</span></span>

<span data-ttu-id="bc86c-117">Os fluxos são usados para evitar o acesso direto ao sistema de arquivos e permitir a escolha do método de análise de XML a ser usado.</span><span class="sxs-lookup"><span data-stu-id="bc86c-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="bc86c-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc86c-118">Examples</span></span>

<span data-ttu-id="bc86c-119">O exemplo a seguir de um manipulador para o evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de um botão cria uma instância da interface de [**interface IJournalReader**](ijournalreader.md) e a usa para ler um arquivo de diário existente.</span><span class="sxs-lookup"><span data-stu-id="bc86c-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a><span data-ttu-id="bc86c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc86c-120">Requirements</span></span>



| <span data-ttu-id="bc86c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc86c-121">Requirement</span></span> | <span data-ttu-id="bc86c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bc86c-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc86c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc86c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc86c-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bc86c-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc86c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc86c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc86c-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bc86c-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="bc86c-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc86c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc86c-128"><dt>Journal. h (também requer Journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bc86c-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bc86c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="bc86c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc86c-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc86c-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="bc86c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc86c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc86c-132">**Interface IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="bc86c-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="bc86c-133">Referência de esquema do leitor de diário</span><span class="sxs-lookup"><span data-stu-id="bc86c-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

