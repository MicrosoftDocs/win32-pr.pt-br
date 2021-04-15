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
# <a name="ijournalreaderreadfromstream-method"></a>Método IJournalReader:: ReadFromStream

Usa um fluxo para um arquivo de anotação do diário e retorna um fluxo XML que representa o conteúdo do documento.

> [!Note]  
> O componente de leitor de diário não pode ler arquivos de diário do Windows criados por computadores que executam o Windows 7 ou posterior. A interface IJournalReader deve ser considerada preterida ou obsoleta e não deve ser usada.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJournalFileStream* \[ no\]
</dt> <dd>

Um objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que representa o arquivo de diário a ser lido.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Um ponteiro para o endereço de um objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que receberá o fluxo XML criado lendo o arquivo de diário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os fluxos são usados para evitar o acesso direto ao sistema de arquivos e permitir a escolha do método de análise de XML a ser usado.

## <a name="examples"></a>Exemplos

O exemplo a seguir de um manipulador para o evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de um botão cria uma instância da interface de [**interface IJournalReader**](ijournalreader.md) e a usa para ler um arquivo de diário existente.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                         |
| parâmetro<br/>                   | <dl> <dt>Journal. h (também requer Journal \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IJournalReader**](ijournalreader.md)
</dt> <dt>

[Referência de esquema do leitor de diário](journal-reader-schema-reference.md)
</dt> </dl>

 

