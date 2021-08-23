---
description: Fornece acesso de leitura a um Windows journal, retornando um fluxo que contém uma versão XML do conteúdo do arquivo.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interface IJournalReader (Journal.h)
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
ms.openlocfilehash: ff0151432e38a3e611e09efe2d5192eefb8c1d3e6cb0e79296e992b728c5a16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590296"
---
# <a name="ijournalreader-interface"></a>Interface IJournalReader

Fornece acesso de leitura a um Windows journal, retornando um fluxo que contém uma versão XML do conteúdo do arquivo.

> [!Note]  
> O componente Leitor de Diário não pode Windows arquivos de Diário criados por máquinas que executam Windows 7 ou posterior. A interface IJournalReader deve ser considerada preterida ou obsoleta e não deve ser usada.

 

## <a name="members"></a>Membros

A interface **IJournalReader** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IJournalReader** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IJournalReader** tem esses métodos.



| Método                                                  | Descrição                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | Leva um fluxo para um arquivo de Anotação de Diário e retorna um fluxo XML que representa o conteúdo do documento.<br/> |



 

## <a name="remarks"></a>Comentários

A **classe JournalReader** permite carregar um fluxo de documentos do Diário e receber um fluxo XML que representa o conteúdo. Você pode reconstituir, exibir e manipular a tinta.

## <a name="examples"></a>Exemplos

O exemplo a seguir de um manipulador para o evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de um botão cria uma instância da classe **JournalReader** e a usa para ler um arquivo de Diário existente.

> [!Note]  
> O **método DisplayXml** chamado deste exemplo não é mostrado. A implementação específica desse método depende das necessidades do aplicativo.

 


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Journal.h (também requer o diário \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GUIDs de propriedade personalizada](custom-property-guids.md)
</dt> <dt>

[**Método ReadFromStream**](ijournalreader-readfromstream.md)
</dt> </dl>

 

