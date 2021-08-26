---
description: Leva um fluxo para um arquivo de Anotação de Diário e retorna um fluxo XML que representa o conteúdo do documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: Método IJournalReader::ReadFromStream (Journal.h)
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
ms.openlocfilehash: 7dbe9d7929f616914d06cad237f486677cd8e5616cb04bf28a5836751ca0a3c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057846"
---
# <a name="ijournalreaderreadfromstream-method"></a>Método IJournalReader::ReadFromStream

Leva um fluxo para um arquivo de Anotação de Diário e retorna um fluxo XML que representa o conteúdo do documento.

> [!Note]  
> O componente Leitor de Diário não pode Windows arquivos de Diário criados por máquinas que executam Windows 7 ou posterior. A interface IJournalReader deve ser considerada preterida ou obsoleta e não deve ser usada.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJournalFileStream* \[ Em\]
</dt> <dd>

Um [**objeto IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que representa o arquivo Journal a ser lido.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Um ponteiro para o endereço de um [**objeto IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que receberá o fluxo XML criado lendo o arquivo Journal.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Fluxos são usados para evitar o acesso direto ao sistema de arquivos e para permitir a escolha em qual método de análise XML usar.

## <a name="examples"></a>Exemplos

O exemplo a seguir de um manipulador para o evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de um botão cria uma instância da [**interface IJournalReader e**](ijournalreader.md) a usa para ler um arquivo de Diário existente.


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
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Journal.h (também requer o diário \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IJournalReader Interface**](ijournalreader.md)
</dt> <dt>

[Referência de esquema de leitor de diário](journal-reader-schema-reference.md)
</dt> </dl>

 

